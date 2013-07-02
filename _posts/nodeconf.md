# NodeConf 2013
ran from Thursday, June 27 to Sunday, June 30w at the outstanding [Walker Creek Ranch](http://www.walkercreekranch.org/) up in Petaluma, and had single handedly the best beer selection and quantity ever encountered at a conference including buckets of both Chimay (Blue & Red) and [Delirium Nocturnum](http://beeradvocate.com/beer/profile/180/1421).

The format was unique. There were 8 workshops that everyone got to attend with unique schedules for all to ensure you were with different people at each workshop. The pre-requisite code for all the workshops was more or less in the [nodeconf2013](https://npmjs.org/package/nodeconf2013) npm package. All of these talks were new-to-node friendly.

There was also Reeses [s'mores](http://en.wikipedia.org/wiki/S'more), watering-hole [swimming](https://en.wikipedia.org/wiki/Human_swimming), multiple near-death diving attempts by me, and very delicious extremely healthy [farm-to-table food](http://en.wikipedia.org/wiki/Farm-to-table). I also got to brag on how much I love LinkedIn and how incredibly awesome my teammates are. Everyone was really excited to hear about what we're doing.

## Workshops:
### [Nodecopter](http://nodecopter.com/):
Hands down the best conference experience I've had in my life. Essentially the [Parrot AR Drone 2.0](http://ardrone2.parrot.com/) creates an ad-hoc wifi network that exposes an API that the node [ar-drone](https://npmjs.org/package/ar-drone) library implements, exposing a REPL and node.js API of it's own. What this means is that you can both control it via REPL AND code. Even cooler, it comes pre-programmed with all sorts of behavior like control over yaw, pitch, roll, lift, rotation, flips, dancing, etc…

The best part about this session was the epiphany regarding the impact of [logic errors](https://en.wikipedia.org/wiki/Logic_error) on hardware programming. In other words, at one point my teammate and I programmed our copter to dance and then flip, but when we realized that flipping for 3 seconds did too many flips, and shortened it to 2, I did not also shorten the dance time to 2 before it, causing the drone to dance for 3s, and then enter into a flip 2s into the dance, causing it to crash hard and impale itself on some hay baler spikes leaning against the barn. More hilarity ensued. Instead of being mortified, the speakers rejoiced in our experimentation and ensuing failure with intense laughter.

### Arduino:
The [johnny-five](https://github.com/rwldrn/johnny-five) node.js module uses the arduino Firmata USB interface to send write node.js programs to control your arduino. I built a circuit that increased an LED's brightness according to the temperature on the thermometer. It was pretty fun playing with circuits and breadboards again. (I was an Electrical Engineer in college)

### Core:
The goal of this session was to do everything necessary to add a function to node.js' C++ and corresponding JavaScript, and the appropriate tests to submit a successful patch. Isaac was excellent in accomplishing this workshop's stated goal. ([Slides](https://github.com/mikeal/nodeconf2013/blob/master/slides/core/how-to-node-core.pdf?raw=true), [Code](https://github.com/mikeal/nodeconf2013/tree/master/slides/core))

### Domains:
Introduction to domains (async error handling) in node.js. If you've ever talked to me about errors in node, you'll know that I have have a lot of experience dealing with errors/domains, possibly more than anyone else (at least on the JavaScript side). It was fairly good, even though what it was teaching was literally in [disagreement with the docs](http://nodejs.org/docs/latest/api/all.html#all_warning_don_t_ignore_errors). Feel free to hit me up for details on the [cognitive](https://github.com/joyent/node/issues/5114) [disonance](https://github.com/joyent/node/issues/5149) that is error handling in node.js. ([Slides](http://othiym23.github.io/nodeconf2013-domains/))

### Streams:
Substack and Max Ogden put together a fantastic game / interactive tutorial of sorts teaching you the basic of streams and incidentally the new streaming API to a degree. [Pipe to your heart's content!](https://npmjs.org/package/stream-adventure )

### Dtrace:
[Dtrace](http://en.wikipedia.org/wiki/DTrace) is a highly performant performance monitoring and debugging tool that was originally built for [SmartOS](http://en.wikipedia.org/wiki/SmartOS) (Joyent's Solaris based OS). It also happens to run on FreeBSD based systems like OSX. No linux yet though, so we cannot run it in production, but for local debugging and performance analysis in node.js, it is unparalleled (albeit very daunting to get started with). Coolest features? Flamegraphs and meta to error (aka C++ to JavaScript) stack traces. ([Slides](http://dtrace.org/blogs/dap/files/2012/07/nodeconf.pdf))

### Web Services:
This was mostly a [Hapi](http://spumko.github.io/) vs [Express](http://expressjs.com/) comparison. Hapi is an exciting framework with a lot of promise, especially since [Flatiron](http://flatironjs.org/) hasn't quite filled the gap like many of us hoped it would. There are some very nice AOP-style request lifetime hooks in Hapi. There's also a nice declarative routing API as well. ([Slides/Code](https://github.com/mikeal/nodeconf2013/tree/master/slides/services))

### Distributed Systems:
The goal here was to implement a peer-to-peer distributed chat app that we found out at the end was actually the implementation of an Amazon white paper, ["Efﬁcient Reconciliation and Flow Control for Anti-Entropy Protocols"](http://www.cs.cornell.edu/home/rvr/papers/flowgossip.pdf). In short, we succeeded. [Distributed Code](https://github.com/Raynos/distributed)
