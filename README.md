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

[nodejs]: http://nodejs.org/download/
[jshint]: http://www.jshint.com/install/
[testem]: https://github.com/airportyh/testem
[grunt]: http://gruntjs.com/getting-started
