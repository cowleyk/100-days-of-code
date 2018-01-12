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
