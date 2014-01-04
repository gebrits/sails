
# Benchmarks

These tests are related to benchmarking the performance of different parts of Sails.  For now, our benchmark tests should be "integration" or "acceptance" tests.  By that, I mean they should measure a specific "user action" (e.g. running `sails new`, running `sails lift`, sending an HTTP request to a dummy endpoint, connecting a Socket.io client, etc.).

> Why test features first, and not functions?
> Those tests are the "lowest-hanging fruit", if you will.

###### Writing good benchmarks
+ Pick what you want to test.
+ Whatever you choose does not have to be atomic (see examples above)-- in an ideal world, we would have benchmarks for every single function in our apps, but that is not how things work today.
+ Write a benchmark test that isolates that functionality. (the hard part)
+ Then see how many miliseconds it takes. (easy)

> Advice from [@felixge](https://github.com/felixge):
>	+ First of all, keep in mind our problems are definitely not the same as Felix's, and we must remember to follow [his own advice](https://github.com/felixge/faster-than-c#taking-performance-advice-from-strangers): `[What]...does not work is taking performance advise (euro-sic) from strangers...`  That said, he's got some great ideas.
>	+ [Benchmark-Driven Optimization](https://github.com/felixge/faster-than-c#benchmark-driven-development)
>	+ I also highly recommend this [talk on optimization and benchmarking](http://2012.jsconf.eu/speaker/2012/09/05/faster-than-c-parsing-node-js-streams-.html) by Felix Geisendörfer ([@felixge](https://github.com/felixge)) ([slides](https://github.com/felixge/faster-than-c)).

