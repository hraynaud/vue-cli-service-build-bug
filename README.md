# README

This is a small app demonstrating what appears to be a bug in the vue-cli v.3
When running npm build withe outputDir set to ./public in vue.config.js
running the The npm run build scripts fails intermittently.  
If the public directory is not present the build is run it will succeed. If yu run the  build again it will fail.  The next time it is run it will succeed and then just alternate between failing and succeeding.



```
Building for production...

 ERROR  Failed to compile with 1 errors                                        11:15:28 PM

  Error: Child compilation failed:
  Entry module not found: Error: Can't resolve '/Users/herbyraynaud/code/personal/vue-cli-  service-build-bug/public/index.html' in '/Users/herbyraynaud/code/personal/vue-cli-servi  ce-build-bug':
  Error: Can't resolve '/Users/herbyraynaud/code/personal/vue-cli-service-build-bug/public  /index.html' in '/Users/herbyraynaud/code/personal/vue-cli-service-build-bug'

  - compiler.js:79 childCompiler.runAsChild
    [vue-cli-service-build-bug]/[html-webpack-plugin]/lib/compiler.js:79:16

  - Compiler.js:300 compile
    [vue-cli-service-build-bug]/[webpack]/lib/Compiler.js:300:11

  - Compiler.js:556 hooks.afterCompile.callAsync.err
    [vue-cli-service-build-bug]/[webpack]/lib/Compiler.js:556:14


  - Hook.js:154 AsyncSeriesHook.lazyCompileHook
    [vue-cli-service-build-bug]/[tapable]/lib/Hook.js:154:20

  - Compiler.js:553 compilation.seal.err
    [vue-cli-service-build-bug]/[webpack]/lib/Compiler.js:553:30


  - Hook.js:154 AsyncSeriesHook.lazyCompileHook
    [vue-cli-service-build-bug]/[tapable]/lib/Hook.js:154:20

  - Compilation.js:1323 hooks.optimizeAssets.callAsync.err
    [vue-cli-service-build-bug]/[webpack]/lib/Compilation.js:1323:35


  - Hook.js:154 AsyncSeriesHook.lazyCompileHook
    [vue-cli-service-build-bug]/[tapable]/lib/Hook.js:154:20

  - Compilation.js:1314 hooks.optimizeChunkAssets.callAsync.err
    [vue-cli-service-build-bug]/[webpack]/lib/Compilation.js:1314:32


  - index.js:319 taskRunner.run
    [vue-cli-service-build-bug]/[terser-webpack-plugin]/dist/index.js:319:9

  - TaskRunner.js:44 TaskRunner.run
    [vue-cli-service-build-bug]/[terser-webpack-plugin]/dist/TaskRunner.js:44:7

  - index.js:225 TerserPlugin.optimizeFn
    [vue-cli-service-build-bug]/[terser-webpack-plugin]/dist/index.js:225:18


* ...
