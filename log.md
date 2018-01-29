# 100 Days Of Code - Log

### Day 1: January 8, Monday

**Today's Goal**: Dev solely in vim. Set up DBs. *Stretch*: Bash script to teardown/remake dbs

**Today's Progress**: Got a chart rendering in UI scaffold. Got initial postgres table set up.

**Thoughts**: New nio binary is causing problems. Need to find help for it. 
Developing in vim is a PITA

**Link(s) to work**
1. n/a

### Day 2: January 9, Tuesday

**Today's Goal**: Pick an API, get block set up, start populating local DB

**Today's Progress**: Discovered super simple GDAX api. Connected and got data I currently want.
 
**Thoughts**: Coinigy/Poloniex APIs seem poorly maintained, 
can successfully curl requests to Coinigy but cannot read JSON responses with Requests library. 
GDAX was awesome and simple and what I want. Going to kick the can down the road and deal with Poloniex || Coinigy 
when I want to start live trading.

### Day 3: January 10, Wednesday

**Today's Goal**: Get service populating local DB, gather historical data for backtesting.
 
**Today's Progress**: Service getting data from GDAX and populating psql DB. Service built to 
pull correct historical data, but don't want to parse "b'[[time, low, high, open, close, volume],...]'"
into an array manually.  Need to figure out what kind of data structure that is.
 
**Thoughts**:  Not starting til 8:30pm, feeling tired.  Should have come home from work, 
ate/walked dog, then started coding.  Went fairly smooth tonight, have a project repo to link. 
90 min flies by. *NEED TO UPDATE PROJECT README*

**Link(s) to work**
1. https://github.com/cowleyk/OneHundredDaysP1

### Day 4: January 11, Thursday

**Today's Goal**: Populate DB with historical data for backtesting

**Today's Progress**: Populated DB with historical data.

**Thoughts**: Used Python's eval(), probably not the best idea but should be fine for my use case. 
Made a super simple block.  I should try to put the real time service in the cloud 
and connect to a cloud db. good opportunity to learn AWS stuff.

**Tomorrow**: Unit tests/documentation for list_split block, start backtesting on December
data.  Maybe set up service to get custom candle intervals for more granular/wider range of data 

**Link(s) to work**
1. https://github.com/cowleyk/OneHundredDaysP1
2. https://github.com/cowleyk/list_split

### Day 5: January 12, Friday

**Today's Goal**: Create block to output trendline data points. Plot w/ plotly block. 
May be helpful to develop in jupyter notebook.

**Today's Progress**: Built MVP of block using numpy's polyfit. Need to be able to compile
array over n signals, but currently will take an array and degree x, calc a x-th degree
polynomial coefficient matrix, and spit out each p(x) for the dependent variables.

**Thoughts**: It's Friday night, didn't get home until 9pm, don't really wanna code. 
Weekends will be the toughest part of this challenge by far.  Didn't use TDD on polynomial
block, wish I would have.

**Tomorrow**: Finish up block (handle stream of prices), plot everything with plotly
start buy sell logic (incorporate volume)  

**Link(s) to work**
1. https://github.com/cowleyk/OneHundredDaysP1
2. https://github.com/cowleyk/list_split
3. https://github.com/cowleyk/polyfit

### Day 6: January 13, Saturday

**Today's Goal**: Finish up polyfit block, plot with plotly, start buy/sell logic.

**Today's Progress**: Polyfit handles streaming data, service will plot price and polyfit line.

**Thoughts**: Made ok progress. Want to see results from polyfit over longer period.  
Thinking about focusing more on backtesting aspect.  Might want to shift to cloud db rather than
writing postgresQuery block?

**Tomorrow**: Calculate +/- stdev of polyfit line (either from block or new block)
Start buy sell logic (incorporate volume)
*FIGURE OUT WHY PLOTLY BLOCK KEEPS MATCHING RANGE(Y-AXIS) WITH RANGE(X-AXIS)*
stretch - ~~AWS~~ Google cloud stuff for cloud db (ultimate goal: host service on raspPi)
stretch.stretch - ~~AWS~~ Google cloud stuff for hosting frontend

**Link(s) to work**
1. https://github.com/cowleyk/OneHundredDaysP1
2. https://github.com/cowleyk/list_split
3. https://github.com/cowleyk/polyfit

### Day 7: January 14, Sunday

**Today's Goals**: Calc +/- stdev line for polynomial, start google cloud db

**Todays Progress**: Polyfit block outputting residual calcs, GoogleSQL cloud db set up
with tables, need to figure out authentication

**Thoughts**:

**Tomorrow**:

**Link(s) to work**
1. https://github.com/cowleyk/OneHundredDaysP1
2. https://github.com/cowleyk/list_split
3. https://github.com/cowleyk/polyfit

### Day 8: January 15, Monday

**Today's Goals**: Connect to google cloud db

**Today's Progress**:  Connected? Maybe? No idea how to implement outside of shell

**Thoughts**:  Frustration. Lethargy. Lack of interest.

**Tomorrow**:

**Link(s) to work**
1. https://github.com/cowleyk/OneHundredDaysP1
2. https://github.com/cowleyk/list_split
3. https://github.com/cowleyk/polyfit

### Day 9: January 16, Tuesday

**Today's Goals**: Connect to google cloud db (try API rather than an engine, will need to provide different creds?) 
Documentation: Blocks, general progress - start doc containing attempts(successful/failures), why I try things, etc
Plan: Revisit outline of blog/app, consider refocusing efforts
Play with ui-scaffold, see if I can't get pubkeeper configured

**Today's Progress**:  Wrote unittests and block documentation.

**Thoughts**:  Didn't make enough time, only went for 30 min.

**Tomorrow**: Back to google cloud

**Link(s) to work**
1. https://github.com/cowleyk/OneHundredDaysP1
2. https://github.com/cowleyk/list_split
3. https://github.com/cowleyk/polyfit

### Day 10: January 17, Wednesday

**Today's Goals**: Connect to google cloud (use API route, ditch engine stuff)

**Today's Progress**:  Decent day!  Connect to google cloud w/ service account credentials
Should be able to utilize psycopg2 from here out once I get a proxy correctly running!

**Thoughts**:  Encouraging end to a frustrating beginning.  The googleapiclient/service
library only lets me manage databases remotely.  Proxy should be first step to actually getting
a block usable w/ the DB.

**Tomorrow**:

**Link(s) to work**
1. https://github.com/cowleyk/OneHundredDaysP1
2. https://github.com/cowleyk/list_split
3. https://github.com/cowleyk/polyfit

### Day 11: January 18, Thursday

**Today's Goals**: Sign and authorize GDAX request

**Today's Progress**: Worked on connecting to API @ meetup.  Learned about what's needed
to execute trades

**Thoughts**:  Light night.

**Tomorrow**: Build out service. UI-Scaffold visualization would be really nice.
Design way to compare current value with buy/sell indicators (state block?)

**Link(s) to work**
1. https://github.com/cowleyk/OneHundredDaysP1
2. https://github.com/cowleyk/list_split
3. https://github.com/cowleyk/polyfit

### Day 12: January 21, Sunday

**Today's Goals**: Sign and authorize GDAX request, build GDAX block.
~~Polyfit block needs to output line + stdevs at t+1, t+2 ...~~ <- build out line on front end

**Today's Progress**: Create service for buy sell logic. 
Need way to filter out noise near stdev lines (debounce blocks?)

**Thoughts**:  Back from weekend break.

**Tomorrow**: Create 'get order' block to grab transaction fee for accounting
Put service onto Pi to have running for a week
*WRITE BLOCK AND SERVICE TESTS*

**Link(s) to work**
1. https://github.com/cowleyk/gdax
2. https://github.com/cowleyk/list_split
3. https://github.com/cowleyk/polyfit

### Day 13: January 22, Monday

**Today's Goals**: Create 'get order' block

**Today's Progress**: Split gdax into base, place_order, and get_order blocks.
 Fiddled with service but not sure why independent/dependent values are getting
 jumbled.

**Thoughts**:  Service seems to be acting up :(

**Tomorrow**: Pue service onto Pi to have running for a week
BRING HOME KEYBOARD
*WRITE BLOCK AND SERVICE TESTS*

**Link(s) to work**
1. https://github.com/cowleyk/gdax
2. https://github.com/cowleyk/list_split
3. https://github.com/cowleyk/polyfit

### Day 14: January 23, Tuesday

**Today's Goals**: Get service functioning properly, unittest blocks

**Today's Progress**:  Confirmed something is wrong on system level w. pub/sub
Will need to create new system
 
**Thoughts**: Struggled with motivation.

**Tomorrow**: See Planning section below
 
**Link(s) to work**
1. https://github.com/cowleyk/gdax
2. https://github.com/cowleyk/list_split
3. https://github.com/cowleyk/polyfit

### Day 15: January 24, Wednesday

**Today's Goals**: Unittest component_environment

**Today's Progress**: Unittest for `handler.py`

**Thoughts**: Worked on work stuff, not true to #100DaysOfCode principles. O well.

**Tomorrow**: See Planning section below

**Link(s) to work**
1. https://github.com/cowleyk/gdax
2. https://github.com/cowleyk/list_split
3. https://github.com/cowleyk/polyfit

### Day 16: January 25, Thursday

**Today's Goals**: *start by posting progress on rockymountaincrypto.slack. A summary will be good to get flowing*
Create new system, verify pub/sub functioning
UI-scaffold attempt
want to make strides on blog tonight. not just unittests or work-work. 

**Today's Progress**: 

**Thoughts**:

**Link(s) to work**
1. https://github.com/cowleyk/gdax
2. https://github.com/cowleyk/list_split
3. https://github.com/cowleyk/polyfit

##Planning
FOCUS ON MVP
- start fresh system
    - ensure pub/sub working
- get gdax & polyfit blocks released
    - would be useful to run it in the cloud
    - OR put it onto my Pi
- post guts on rockymountaincrypto.slack
- decide on time intervals
    - what's reasonable for data processing? Should polyfit just spit out coefficients?
        - *really only need most recent value for comparison. should calc arrays on front end*
        - Run polyfit calcs 1/day for last x days/weeks, have socket stream set up to continuously check values
            - store most recent coefficients as state
            - would be good idea to run calcs w/ multiple intervals, compare residuals and pick most linear interval
- change stdev lines to +/- sqrt(residual/n)
    - residual = sum of squares of fit errors
- Need retry/delay logic to check orders AFTER they are filled (want to get actual fill data)
- some sort of visualization would be very useful (necessary) to actually blog it
- Switch polyfit block to use OLS from statsmodels
    - http://www.statsmodels.org/stable/examples/notebooks/generated/ols.html
- GDAX socket block using https://github.com/danpaquin/gdax-python/blob/master/gdax/websocket_client.py
- Check out https://github.com/ccxt/ccxt