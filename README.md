# npmdoc-watson-developer-cloud

#### basic api documentation for  [watson-developer-cloud (v2.29.0)](https://github.com/watson-developer-cloud/node-sdk#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-watson-developer-cloud.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-watson-developer-cloud) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-watson-developer-cloud.svg)](https://travis-ci.org/npmdoc/node-npmdoc-watson-developer-cloud)

#### Client library to use the IBM Watson Services and AlchemyAPI

[![NPM](https://nodei.co/npm/watson-developer-cloud.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/watson-developer-cloud)

- [https://npmdoc.github.io/node-npmdoc-watson-developer-cloud/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-watson-developer-cloud/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-watson-developer-cloud/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-watson-developer-cloud/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-watson-developer-cloud/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-watson-developer-cloud/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "IBM Corp."
    },
    "bugs": {
        "url": "https://github.com/watson-developer-cloud/node-sdk/issues"
    },
    "contributors": [
        {
            "name": "German Attanasio Ruiz"
        },
        {
            "name": "Nathan Friedly"
        },
        {
            "name": "Jeff Stylos"
        }
    ],
    "dependencies": {
        "async": "^2.0.1",
        "buffer-from": "^0.1.1",
        "cookie": "~0.3.1",
        "csv-stringify": "~1.0.2",
        "extend": "~3.0.0",
        "isstream": "~0.1.2",
        "object.omit": "~2.0.0",
        "object.pick": "~1.2.0",
        "request": "~2.81.0",
        "solr-client": "~0.6.0",
        "string": "3.3.3",
        "vcap_services": "~0.3.0",
        "websocket": "~1.0.22"
    },
    "description": "Client library to use the IBM Watson Services and AlchemyAPI",
    "devDependencies": {
        "browserify": "^14.0.0",
        "concat-stream": "^1.5.1",
        "dependency-lint": "^5.0.1",
        "eslint": "^3.14.1",
        "eslint-config-google": "^0.7.1",
        "eslint-config-prettier": "git+https://github.com/nfriedly/eslint-config-prettier.git#nfriedly-patch-1",
        "eslint-plugin-node": "^4.0.0",
        "eslint-plugin-prettier": "^2.0.0",
        "jsdoc": "^3.4.0",
        "karma": "^1.1.1",
        "karma-browserify": "^5.0.5",
        "karma-chrome-launcher": "^2.0.0",
        "karma-firefox-launcher": "^1.0.0",
        "karma-mocha": "^1.1.1",
        "memory-fs": "^0.4.1",
        "mocha": "^3.2.0",
        "nock": "^9.0.2",
        "object.assign": "^4.0.4",
        "prettier": "^1.1.0",
        "shebang-loader": "0.0.1",
        "uglify-js": "^2.7.0",
        "watchify": "^3.7.0",
        "wav": "^1.0.0",
        "webpack": "^2.2.1"
    },
    "directories": {},
    "dist": {
        "shasum": "4a343a8dc3116113ce8b6d047f62470c60183ac5",
        "tarball": "https://registry.npmjs.org/watson-developer-cloud/-/watson-developer-cloud-2.29.0.tgz"
    },
    "engines": {
        "node": ">=4"
    },
    "gitHead": "7f4ad30a69f6994b930df2f464f7f4a7bf6fb792",
    "homepage": "https://github.com/watson-developer-cloud/node-sdk#readme",
    "keywords": [
        "ibm",
        "watson",
        "wdc",
        "watson developer cloud",
        "chatbot",
        "message resonance",
        "user modeling",
        "dialog",
        "personality insights",
        "machine translation",
        "concept expansion",
        "question and answer",
        "relationship extraction",
        "language identification",
        "language translation",
        "visual recognition ",
        "speech to text",
        "text to speech",
        "concept insights",
        "tradeoff analytics",
        "tone analyzer",
        "retrieve and rank",
        "natural language classifier",
        "dialog",
        "tone_analyzer",
        "alchemy",
        "alchemyapi",
        "alchemy vision",
        "alchemy language",
        "alchemy datanews",
        "conversation"
    ],
    "license": "Apache-2.0",
    "main": "./index",
    "maintainers": [
        {
            "name": "germanattanasio"
        },
        {
            "name": "kognate"
        },
        {
            "name": "nfriedly"
        }
    ],
    "name": "watson-developer-cloud",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git+https://github.com/watson-developer-cloud/node-sdk.git"
    },
    "scripts": {
        "autofix": "eslint . --fix",
        "browserify": "browserify index.js --standalone Watson --outfile dist/watson.js",
        "build": "npm run browserify && npm run minify",
        "compat-check": "eslint --print-config .eslintrc.js | eslint-config-prettier-check",
        "doc": "jsdoc -c scripts/jsdoc/config.json",
        "lint": "npm run compat-check && eslint . --cache && dependency-lint",
        "minify": "uglifyjs --compress --mangle --screw-ie8 dist/watson.js --output dist/watson.min.js --preamble \"// Watson Developer Cloud\n// JavaScript SDK$npm_package_version\n// Generated at 'date'\n// Copyright IBM ($npm_package_license)\n// $npm_package_homepage\"",
        "test": "npm run lint && mocha test/unit test/integration",
        "test-browser": "karma start --single-run",
        "test-integration": "mocha test/integration",
        "test-unit": "npm run lint && mocha test/unit/",
        "watch": "npm run test-unit -- --watch",
        "watch-doc": "nodemon --watch ./ --ext js,tmpl,json --ignore dist/ --ignore doc/ --ignore test/ --ignore examples/ --exec npm run doc",
        "watchify": "watchify index.js --standalone Watson --outfile dist/watson.js --debug --verbose"
    },
    "version": "2.29.0",
    "bin": {}
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
