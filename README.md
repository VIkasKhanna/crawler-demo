# crawler-demo
Simple demonstration of node js spider code using recursive method to crawl with test cases and demo running on express. 
User set options.startUrl url as entry point and userCallback method which will be invoked with output.json as param.
  
  # Get started

## Install

```sh
download zip or clone the source code
```
from working folder 
```js
$ npm install 
```
above will download required node plugins.
## Basic usage

```js

var options = {
  crawlLimit: 0,
  inDomainOnly: true,
  startUrl:"http://localhost:3000/",
  userCallback:handleSpiderOutput,
  skipDuplicates:true,
}
console.clear();


var Spider = require('./lib/spider');
spider = new Spider(options);
// spider();
spider.crawl();

## running demo 
start web express server  
$ node server.js

start demo  in diff console , this will generate output.json
$ node demo.js
//this will save output.json in working directory.

Set crawl url 
    options.StartUrl

Set crawllimit more than 0 to limit page requests
    options.crawlLimit

## TEST 
$ npm test
