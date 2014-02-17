## Getting Started

### Install prerequisites

* Install [nodejs][nodejs]
  (mac ```brew install nodejs``` windows ```cinst nodejs```)
* Install [jshint][jshint] and get jshint running in your favorite editor
  ```npm install -g jshint```
* Install [testem][testem] ```npm install -g testem```
* install [grunt][grunt] ```npm install -g grunt-cli```


### Create your directory structure

* ```mkdir -p js-meetup-testing/{src,test} && cd js-meetup-testing```
* create a .testem file with the following content

```
{
  "framework": "qunit",
  "src_files": [
    "src/*.js",
    "test/**/*-test.js"
  ]
}
```

* fire up testem and lets get cooking! ```testem```

### Hello World Test

```javascript
window.helloWorld = function (name) {
  return "Hello " + name + "!";
}

test('hello world says hello', function (assert) {
  var result = helloWorld('dan');
  assert.equal("Hello dan!", result);
});
```

[QUnit Assertions][qunit_assertions]


### Launchers

* ```testem launchers``` to see the list of launchers
* include the ```launch_in_dev``` key to identify dev launchers
* run ```testem``` and watch the launchers

### Include jQuery

* ```mkdir vendor && cd vendor```
* ```curl http://code.jquery.com/jquery-2.1.0.js -O```
* ```cd ..```
* add ```vendor/jquery-2.1.0.js``` to the ```.testem.json``` src_files.


[nodejs]: http://nodejs.org/download/
[jshint]: http://www.jshint.com/install/
[testem]: https://github.com/airportyh/testem
[grunt]: http://gruntjs.com/getting-started
[qunit_assertions]: http://api.qunitjs.com/category/assert/
