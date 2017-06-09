# awesome-deopt

> with [nodejs v8](https://nodejs.org/en/blog/release/v8.0.0/), there is some new fun stuff for finding deopts, alongside existing ways to view them easily in chrome.

## TL;DR

#### browser
- [clone chromium deopt_tools](https://www.chromium.org/developers/how-tos/run-chromium-with-flags) `git clone https://chromium.googlesource.com/chromium/tools/depot_tools.git` ([optionally export the $PATH](https://www.cyberciti.biz/faq/appleosx-bash-unix-change-set-path-environment-variable/))
- [download chromium, put in Applications](https://www.chromium.org/getting-involved/download-chromium)
- [run chromium with some flags](https://www.chromium.org/developers/how-tos/run-chromium-with-flags) `/Applications/Chromium.app/Contents/MacOS/Chromium --remote-debugging-port=9222 --js-flags="--trace-opt --trace-deopt"`

#### node 8+
- [use nvm](https://github.com/creationix/nvm) to install [nodejs v8](https://nodejs.org/en/blog/release/v8.0.0/) (`nvm install 8.1 && nvm alias default 8.1 && nvm use 8.1`)
- run `node prof YOUR_FILE_HERE`, then `node --prof-process isolate-TAB_AUTO_COMPLETE_HERE`
- [run using chrome devtools](https://medium.com/@paul_irish/debugging-node-js-nightlies-with-chrome-devtools-7c4a1b95ae27) `node --inspect --debug-brk YOUR_FILE_HERE`

----

### must read
- https://twitter.com/bmeurer/status/870647864329981952 (this has everything you need, thanks @trueadm)


### tools / short how-tos
- https://www.chromium.org/developers/how-tos/run-chromium-with-flags
- https://gist.github.com/kevincennis/0cd2138c78a07412ef21
- http://peter.sh/experiments/chromium-command-line-switches/

### articles

#### newer
- https://v8project.blogspot.ca/2017/05/launching-ignition-and-turbofan.html
- https://v8project.blogspot.ca/2016/08/firing-up-ignition-interpreter.html
- https://hackernoon.com/debug-node-js-with-chrome-devtools-aca7cf83af6b
- https://medium.com/@paul_irish/debugging-node-js-nightlies-with-chrome-devtools-7c4a1b95ae27
- https://insight.io/github.com/nodejs/node/blob/master/deps/v8/src/crankshaft/hydrogen-check-elimination.cc
- http://benediktmeurer.de/2017/03/01/v8-behind-the-scenes-february-edition/
- https://github.com/vhf/v8-bailout-reasons

#### older
- https://news.ycombinator.com/item?id=14373885
- https://github.com/petkaantonov/bluebird/wiki/Optimization-killers
- https://developers.google.com/v8/profiler_example
- http://www.mattzeunert.com/2015/08/19/viewing-assembly-code-generated-by-v8.html
- https://github.com/nodejs/diagnostics/tree/master/tracing/AsyncWrap
- http://mrale.ph/irhydra/2/
- https://github.com/thlorenz/v8-perf/blob/master/performance-profiling.md
- https://blog.ghaiklor.com/tracing-de-optimizations-in-nodejs-2ba16900fc6f
- https://stackoverflow.com/questions/21357963/nodejs-profiling-what-to-do-with-v8-log-file
- http://www.mattzeunert.com/2015/08/19/viewing-assembly-code-generated-by-v8.html
- https://kripken.github.io/emscripten-site/docs/optimizing/Optimizing-Code.html
- https://community.risingstack.com/how-to-find-node-js-performance-optimization-killers/

### misc
- https://github.com/v8/v8/blob/master/tools/profview/index.html
- https://nodejs.org/api/tracing.html
- https://github.com/fluents/bench-chain
- http://perf.rocks/tools/
- https://github.com/sidorares/node-tick
- https://github.com/node-inspector/node-inspector
- https://github.com/RisingStack/trace-nodejs
- https://nodejs.org/api/cli.html
- https://github.com/nodejs/node/tree/master/benchmark
