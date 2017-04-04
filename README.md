# api documentation for  [watson-developer-cloud (v2.28.0)](https://github.com/watson-developer-cloud/node-sdk#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-watson-developer-cloud.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-watson-developer-cloud) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-watson-developer-cloud.svg)](https://travis-ci.org/npmdoc/node-npmdoc-watson-developer-cloud)
#### Client library to use the IBM Watson Services and AlchemyAPI

[![NPM](https://nodei.co/npm/watson-developer-cloud.png?downloads=true)](https://www.npmjs.com/package/watson-developer-cloud)

[![apidoc](https://npmdoc.github.io/node-npmdoc-watson-developer-cloud/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-watson-developer-cloud_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-watson-developer-cloud/build/apidoc.html)

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
            "name": "German Attanasio Ruiz",
            "email": "germanatt@us.ibm.com"
        },
        {
            "name": "Nathan Friedly",
            "email": "nfriedly@us.ibm.com"
        },
        {
            "name": "Jeff Stylos",
            "email": "jsstylos@us.ibm.com"
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
        "request": "~2.79.0",
        "solr-client": "~0.6.0",
        "string": "3.3.3",
        "vcap_services": "~0.3.0",
        "websocket": "~1.0.22"
    },
    "description": "Client library to use the IBM Watson Services and AlchemyAPI",
    "devDependencies": {
        "browserify": "^14.0.0",
        "concat-stream": "^1.5.1",
        "dependency-lint": "^4.2.0",
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
        "prettier": "^0.18.0",
        "shebang-loader": "0.0.1",
        "uglify-js": "^2.7.0",
        "watchify": "^3.7.0",
        "wav": "^1.0.0",
        "webpack": "^2.2.1"
    },
    "directories": {},
    "dist": {
        "shasum": "6f01970e8437ca6547194c82bdf044e2fb123172",
        "tarball": "https://registry.npmjs.org/watson-developer-cloud/-/watson-developer-cloud-2.28.0.tgz"
    },
    "engines": {
        "node": ">=4"
    },
    "gitHead": "7d2e2165b0e233a086aea53535c2a088c494e9b8",
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
            "name": "germanattanasio",
            "email": "germanattanasio@gmail.com"
        },
        {
            "name": "kognate",
            "email": "kognate@gmail.com"
        },
        {
            "name": "nfriedly",
            "email": "nathan@nfriedly.com"
        }
    ],
    "name": "watson-developer-cloud",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
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
    "version": "2.28.0"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module watson-developer-cloud](#apidoc.module.watson-developer-cloud)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.</span>AlchemyDataNewsV1 (options)](#apidoc.element.watson-developer-cloud.AlchemyDataNewsV1)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.</span>AlchemyDataNewsV1.super_ (options)](#apidoc.element.watson-developer-cloud.AlchemyDataNewsV1.super_)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.</span>AlchemyLanguageV1 (options)](#apidoc.element.watson-developer-cloud.AlchemyLanguageV1)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.</span>AlchemyVisionV1 (options)](#apidoc.element.watson-developer-cloud.AlchemyVisionV1)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.</span>AuthorizationV1 (options)](#apidoc.element.watson-developer-cloud.AuthorizationV1)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.</span>AuthorizationV1.super_ (user_options)](#apidoc.element.watson-developer-cloud.AuthorizationV1.super_)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.</span>ConversationV1 (options)](#apidoc.element.watson-developer-cloud.ConversationV1)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.</span>ConversationV1Experimental (options)](#apidoc.element.watson-developer-cloud.ConversationV1Experimental)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.</span>DialogV1 (options)](#apidoc.element.watson-developer-cloud.DialogV1)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.</span>DiscoveryV1 (options)](#apidoc.element.watson-developer-cloud.DiscoveryV1)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.</span>DiscoveryV1Experimental (options)](#apidoc.element.watson-developer-cloud.DiscoveryV1Experimental)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.</span>DocumentConversionV1 (options)](#apidoc.element.watson-developer-cloud.DocumentConversionV1)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.</span>LanguageTranslationV2 (options)](#apidoc.element.watson-developer-cloud.LanguageTranslationV2)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.</span>LanguageTranslatorV2 (options)](#apidoc.element.watson-developer-cloud.LanguageTranslatorV2)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.</span>NaturalLanguageClassifierV1 (options)](#apidoc.element.watson-developer-cloud.NaturalLanguageClassifierV1)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.</span>NaturalLanguageUnderstandingV1 (options)](#apidoc.element.watson-developer-cloud.NaturalLanguageUnderstandingV1)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.</span>PersonalityInsightsV2 (options)](#apidoc.element.watson-developer-cloud.PersonalityInsightsV2)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.</span>PersonalityInsightsV3 (options)](#apidoc.element.watson-developer-cloud.PersonalityInsightsV3)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.</span>RetrieveAndRankV1 (options)](#apidoc.element.watson-developer-cloud.RetrieveAndRankV1)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.</span>SpeechToTextV1 (options)](#apidoc.element.watson-developer-cloud.SpeechToTextV1)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.</span>TextToSpeechV1 (options)](#apidoc.element.watson-developer-cloud.TextToSpeechV1)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.</span>ToneAnalyzerV3 (options)](#apidoc.element.watson-developer-cloud.ToneAnalyzerV3)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.</span>TradeoffAnalyticsV1 (options)](#apidoc.element.watson-developer-cloud.TradeoffAnalyticsV1)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.</span>VisualRecognitionV3 (options)](#apidoc.element.watson-developer-cloud.VisualRecognitionV3)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.</span>recognize_stream (options)](#apidoc.element.watson-developer-cloud.recognize_stream)
1.  object <span class="apidocSignatureSpan">watson-developer-cloud.</span>AlchemyDataNewsV1.prototype
1.  object <span class="apidocSignatureSpan">watson-developer-cloud.</span>AlchemyDataNewsV1.super_.prototype
1.  object <span class="apidocSignatureSpan">watson-developer-cloud.</span>AlchemyLanguageV1.prototype
1.  object <span class="apidocSignatureSpan">watson-developer-cloud.</span>AlchemyVisionV1.prototype
1.  object <span class="apidocSignatureSpan">watson-developer-cloud.</span>AuthorizationV1.prototype
1.  object <span class="apidocSignatureSpan">watson-developer-cloud.</span>AuthorizationV1.super_.prototype
1.  object <span class="apidocSignatureSpan">watson-developer-cloud.</span>ConversationV1.prototype
1.  object <span class="apidocSignatureSpan">watson-developer-cloud.</span>ConversationV1Experimental.prototype
1.  object <span class="apidocSignatureSpan">watson-developer-cloud.</span>DialogV1.prototype
1.  object <span class="apidocSignatureSpan">watson-developer-cloud.</span>DiscoveryV1.prototype
1.  object <span class="apidocSignatureSpan">watson-developer-cloud.</span>DiscoveryV1Experimental.prototype
1.  object <span class="apidocSignatureSpan">watson-developer-cloud.</span>DocumentConversionV1.prototype
1.  object <span class="apidocSignatureSpan">watson-developer-cloud.</span>LanguageTranslationV2.prototype
1.  object <span class="apidocSignatureSpan">watson-developer-cloud.</span>LanguageTranslatorV2.prototype
1.  object <span class="apidocSignatureSpan">watson-developer-cloud.</span>NaturalLanguageClassifierV1.prototype
1.  object <span class="apidocSignatureSpan">watson-developer-cloud.</span>NaturalLanguageUnderstandingV1.prototype
1.  object <span class="apidocSignatureSpan">watson-developer-cloud.</span>PersonalityInsightsV2.prototype
1.  object <span class="apidocSignatureSpan">watson-developer-cloud.</span>PersonalityInsightsV3.prototype
1.  object <span class="apidocSignatureSpan">watson-developer-cloud.</span>RetrieveAndRankV1.prototype
1.  object <span class="apidocSignatureSpan">watson-developer-cloud.</span>SpeechToTextV1.prototype
1.  object <span class="apidocSignatureSpan">watson-developer-cloud.</span>TextToSpeechV1.prototype
1.  object <span class="apidocSignatureSpan">watson-developer-cloud.</span>ToneAnalyzerV3.prototype
1.  object <span class="apidocSignatureSpan">watson-developer-cloud.</span>TradeoffAnalyticsV1.prototype
1.  object <span class="apidocSignatureSpan">watson-developer-cloud.</span>VisualRecognitionV3.prototype
1.  object <span class="apidocSignatureSpan">watson-developer-cloud.</span>helper
1.  object <span class="apidocSignatureSpan">watson-developer-cloud.</span>recognize_stream.prototype

#### [module watson-developer-cloud.AlchemyDataNewsV1](#apidoc.module.watson-developer-cloud.AlchemyDataNewsV1)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.</span>AlchemyDataNewsV1 (options)](#apidoc.element.watson-developer-cloud.AlchemyDataNewsV1.AlchemyDataNewsV1)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.AlchemyDataNewsV1.</span>super_ (options)](#apidoc.element.watson-developer-cloud.AlchemyDataNewsV1.super_)
1.  string <span class="apidocSignatureSpan">watson-developer-cloud.AlchemyDataNewsV1.</span>URL

#### [module watson-developer-cloud.AlchemyDataNewsV1.prototype](#apidoc.module.watson-developer-cloud.AlchemyDataNewsV1.prototype)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.AlchemyDataNewsV1.prototype.</span>getNews (params, callback)](#apidoc.element.watson-developer-cloud.AlchemyDataNewsV1.prototype.getNews)
1.  string <span class="apidocSignatureSpan">watson-developer-cloud.AlchemyDataNewsV1.prototype.</span>name
1.  string <span class="apidocSignatureSpan">watson-developer-cloud.AlchemyDataNewsV1.prototype.</span>version

#### [module watson-developer-cloud.AlchemyDataNewsV1.super_](#apidoc.module.watson-developer-cloud.AlchemyDataNewsV1.super_)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.AlchemyDataNewsV1.</span>super_ (user_options)](#apidoc.element.watson-developer-cloud.AlchemyDataNewsV1.super_.super_)

#### [module watson-developer-cloud.AlchemyDataNewsV1.super_.prototype](#apidoc.module.watson-developer-cloud.AlchemyDataNewsV1.super_.prototype)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.AlchemyDataNewsV1.super_.prototype.</span>getCredentials ()](#apidoc.element.watson-developer-cloud.AlchemyDataNewsV1.super_.prototype.getCredentials)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.AlchemyDataNewsV1.super_.prototype.</span>getCredentialsFromEnvironment (name)](#apidoc.element.watson-developer-cloud.AlchemyDataNewsV1.super_.prototype.getCredentialsFromEnvironment)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.AlchemyDataNewsV1.super_.prototype.</span>initCredentials (options)](#apidoc.element.watson-developer-cloud.AlchemyDataNewsV1.super_.prototype.initCredentials)

#### [module watson-developer-cloud.AlchemyLanguageV1](#apidoc.module.watson-developer-cloud.AlchemyLanguageV1)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.</span>AlchemyLanguageV1 (options)](#apidoc.element.watson-developer-cloud.AlchemyLanguageV1.AlchemyLanguageV1)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.AlchemyLanguageV1.</span>super_ (options)](#apidoc.element.watson-developer-cloud.AlchemyLanguageV1.super_)
1.  string <span class="apidocSignatureSpan">watson-developer-cloud.AlchemyLanguageV1.</span>URL

#### [module watson-developer-cloud.AlchemyLanguageV1.prototype](#apidoc.module.watson-developer-cloud.AlchemyLanguageV1.prototype)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.AlchemyLanguageV1.prototype.</span>authors (_params, callback)](#apidoc.element.watson-developer-cloud.AlchemyLanguageV1.prototype.authors)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.AlchemyLanguageV1.prototype.</span>category (_params, callback)](#apidoc.element.watson-developer-cloud.AlchemyLanguageV1.prototype.category)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.AlchemyLanguageV1.prototype.</span>combined (_params, callback)](#apidoc.element.watson-developer-cloud.AlchemyLanguageV1.prototype.combined)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.AlchemyLanguageV1.prototype.</span>concepts (_params, callback)](#apidoc.element.watson-developer-cloud.AlchemyLanguageV1.prototype.concepts)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.AlchemyLanguageV1.prototype.</span>dates (_params, callback)](#apidoc.element.watson-developer-cloud.AlchemyLanguageV1.prototype.dates)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.AlchemyLanguageV1.prototype.</span>emotion (params, callback)](#apidoc.element.watson-developer-cloud.AlchemyLanguageV1.prototype.emotion)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.AlchemyLanguageV1.prototype.</span>entities (_params, callback)](#apidoc.element.watson-developer-cloud.AlchemyLanguageV1.prototype.entities)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.AlchemyLanguageV1.prototype.</span>feeds (_params, callback)](#apidoc.element.watson-developer-cloud.AlchemyLanguageV1.prototype.feeds)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.AlchemyLanguageV1.prototype.</span>keywords (_params, callback)](#apidoc.element.watson-developer-cloud.AlchemyLanguageV1.prototype.keywords)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.AlchemyLanguageV1.prototype.</span>language (_params, callback)](#apidoc.element.watson-developer-cloud.AlchemyLanguageV1.prototype.language)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.AlchemyLanguageV1.prototype.</span>microformats (_params, callback)](#apidoc.element.watson-developer-cloud.AlchemyLanguageV1.prototype.microformats)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.AlchemyLanguageV1.prototype.</span>publicationDate (_params, callback)](#apidoc.element.watson-developer-cloud.AlchemyLanguageV1.prototype.publicationDate)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.AlchemyLanguageV1.prototype.</span>relations (_params, callback)](#apidoc.element.watson-developer-cloud.AlchemyLanguageV1.prototype.relations)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.AlchemyLanguageV1.prototype.</span>sentiment (params, callback)](#apidoc.element.watson-developer-cloud.AlchemyLanguageV1.prototype.sentiment)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.AlchemyLanguageV1.prototype.</span>taxonomy (_params, callback)](#apidoc.element.watson-developer-cloud.AlchemyLanguageV1.prototype.taxonomy)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.AlchemyLanguageV1.prototype.</span>text (params, callback)](#apidoc.element.watson-developer-cloud.AlchemyLanguageV1.prototype.text)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.AlchemyLanguageV1.prototype.</span>title (_params, callback)](#apidoc.element.watson-developer-cloud.AlchemyLanguageV1.prototype.title)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.AlchemyLanguageV1.prototype.</span>typedRelations (_params, callback)](#apidoc.element.watson-developer-cloud.AlchemyLanguageV1.prototype.typedRelations)
1.  string <span class="apidocSignatureSpan">watson-developer-cloud.AlchemyLanguageV1.prototype.</span>name
1.  string <span class="apidocSignatureSpan">watson-developer-cloud.AlchemyLanguageV1.prototype.</span>version

#### [module watson-developer-cloud.AlchemyVisionV1](#apidoc.module.watson-developer-cloud.AlchemyVisionV1)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.</span>AlchemyVisionV1 (options)](#apidoc.element.watson-developer-cloud.AlchemyVisionV1.AlchemyVisionV1)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.AlchemyVisionV1.</span>super_ (options)](#apidoc.element.watson-developer-cloud.AlchemyVisionV1.super_)
1.  string <span class="apidocSignatureSpan">watson-developer-cloud.AlchemyVisionV1.</span>URL

#### [module watson-developer-cloud.AlchemyVisionV1.prototype](#apidoc.module.watson-developer-cloud.AlchemyVisionV1.prototype)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.AlchemyVisionV1.prototype.</span>getImageKeywords (_params, callback)](#apidoc.element.watson-developer-cloud.AlchemyVisionV1.prototype.getImageKeywords)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.AlchemyVisionV1.prototype.</span>getImageLinks (_params, callback)](#apidoc.element.watson-developer-cloud.AlchemyVisionV1.prototype.getImageLinks)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.AlchemyVisionV1.prototype.</span>getImageSceneText (_params, callback)](#apidoc.element.watson-developer-cloud.AlchemyVisionV1.prototype.getImageSceneText)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.AlchemyVisionV1.prototype.</span>recognizeFaces (_params, callback)](#apidoc.element.watson-developer-cloud.AlchemyVisionV1.prototype.recognizeFaces)
1.  string <span class="apidocSignatureSpan">watson-developer-cloud.AlchemyVisionV1.prototype.</span>name
1.  string <span class="apidocSignatureSpan">watson-developer-cloud.AlchemyVisionV1.prototype.</span>version

#### [module watson-developer-cloud.AuthorizationV1](#apidoc.module.watson-developer-cloud.AuthorizationV1)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.</span>AuthorizationV1 (options)](#apidoc.element.watson-developer-cloud.AuthorizationV1.AuthorizationV1)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.AuthorizationV1.</span>super_ (user_options)](#apidoc.element.watson-developer-cloud.AuthorizationV1.super_)
1.  string <span class="apidocSignatureSpan">watson-developer-cloud.AuthorizationV1.</span>URL

#### [module watson-developer-cloud.AuthorizationV1.prototype](#apidoc.module.watson-developer-cloud.AuthorizationV1.prototype)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.AuthorizationV1.prototype.</span>getToken (params, callback)](#apidoc.element.watson-developer-cloud.AuthorizationV1.prototype.getToken)
1.  string <span class="apidocSignatureSpan">watson-developer-cloud.AuthorizationV1.prototype.</span>name
1.  string <span class="apidocSignatureSpan">watson-developer-cloud.AuthorizationV1.prototype.</span>version

#### [module watson-developer-cloud.AuthorizationV1.super_](#apidoc.module.watson-developer-cloud.AuthorizationV1.super_)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.AuthorizationV1.</span>super_ (user_options)](#apidoc.element.watson-developer-cloud.AuthorizationV1.super_.super_)

#### [module watson-developer-cloud.AuthorizationV1.super_.prototype](#apidoc.module.watson-developer-cloud.AuthorizationV1.super_.prototype)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.AuthorizationV1.super_.prototype.</span>getCredentials ()](#apidoc.element.watson-developer-cloud.AuthorizationV1.super_.prototype.getCredentials)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.AuthorizationV1.super_.prototype.</span>getCredentialsFromBluemix (vcap_services_name)](#apidoc.element.watson-developer-cloud.AuthorizationV1.super_.prototype.getCredentialsFromBluemix)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.AuthorizationV1.super_.prototype.</span>getCredentialsFromEnvironment (name)](#apidoc.element.watson-developer-cloud.AuthorizationV1.super_.prototype.getCredentialsFromEnvironment)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.AuthorizationV1.super_.prototype.</span>initCredentials (options)](#apidoc.element.watson-developer-cloud.AuthorizationV1.super_.prototype.initCredentials)

#### [module watson-developer-cloud.ConversationV1](#apidoc.module.watson-developer-cloud.ConversationV1)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.</span>ConversationV1 (options)](#apidoc.element.watson-developer-cloud.ConversationV1.ConversationV1)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.ConversationV1.</span>super_ (user_options)](#apidoc.element.watson-developer-cloud.ConversationV1.super_)
1.  string <span class="apidocSignatureSpan">watson-developer-cloud.ConversationV1.</span>URL
1.  string <span class="apidocSignatureSpan">watson-developer-cloud.ConversationV1.</span>VERSION_DATE_2016_07_11
1.  string <span class="apidocSignatureSpan">watson-developer-cloud.ConversationV1.</span>VERSION_DATE_2016_09_20
1.  string <span class="apidocSignatureSpan">watson-developer-cloud.ConversationV1.</span>VERSION_DATE_2017_02_03

#### [module watson-developer-cloud.ConversationV1.prototype](#apidoc.module.watson-developer-cloud.ConversationV1.prototype)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.ConversationV1.prototype.</span>createCounterExample (params, callback)](#apidoc.element.watson-developer-cloud.ConversationV1.prototype.createCounterExample)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.ConversationV1.prototype.</span>createExample (params, callback)](#apidoc.element.watson-developer-cloud.ConversationV1.prototype.createExample)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.ConversationV1.prototype.</span>createIntent (params, callback)](#apidoc.element.watson-developer-cloud.ConversationV1.prototype.createIntent)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.ConversationV1.prototype.</span>createWorkspace (params, callback)](#apidoc.element.watson-developer-cloud.ConversationV1.prototype.createWorkspace)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.ConversationV1.prototype.</span>deleteCounterExample (params, callback)](#apidoc.element.watson-developer-cloud.ConversationV1.prototype.deleteCounterExample)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.ConversationV1.prototype.</span>deleteExample (params, callback)](#apidoc.element.watson-developer-cloud.ConversationV1.prototype.deleteExample)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.ConversationV1.prototype.</span>deleteIntent (params, callback)](#apidoc.element.watson-developer-cloud.ConversationV1.prototype.deleteIntent)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.ConversationV1.prototype.</span>deleteWorkspace (params, callback)](#apidoc.element.watson-developer-cloud.ConversationV1.prototype.deleteWorkspace)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.ConversationV1.prototype.</span>getCounterExample (params, callback)](#apidoc.element.watson-developer-cloud.ConversationV1.prototype.getCounterExample)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.ConversationV1.prototype.</span>getCounterExamples (params, callback)](#apidoc.element.watson-developer-cloud.ConversationV1.prototype.getCounterExamples)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.ConversationV1.prototype.</span>getExample (params, callback)](#apidoc.element.watson-developer-cloud.ConversationV1.prototype.getExample)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.ConversationV1.prototype.</span>getExamples (params, callback)](#apidoc.element.watson-developer-cloud.ConversationV1.prototype.getExamples)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.ConversationV1.prototype.</span>getIntent (params, callback)](#apidoc.element.watson-developer-cloud.ConversationV1.prototype.getIntent)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.ConversationV1.prototype.</span>getIntents (params, callback)](#apidoc.element.watson-developer-cloud.ConversationV1.prototype.getIntents)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.ConversationV1.prototype.</span>getWorkspace (params, callback)](#apidoc.element.watson-developer-cloud.ConversationV1.prototype.getWorkspace)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.ConversationV1.prototype.</span>listWorkspaces (params, callback)](#apidoc.element.watson-developer-cloud.ConversationV1.prototype.listWorkspaces)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.ConversationV1.prototype.</span>message (params, callback)](#apidoc.element.watson-developer-cloud.ConversationV1.prototype.message)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.ConversationV1.prototype.</span>updateCounterExample (params, callback)](#apidoc.element.watson-developer-cloud.ConversationV1.prototype.updateCounterExample)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.ConversationV1.prototype.</span>updateExample (params, callback)](#apidoc.element.watson-developer-cloud.ConversationV1.prototype.updateExample)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.ConversationV1.prototype.</span>updateIntent (params, callback)](#apidoc.element.watson-developer-cloud.ConversationV1.prototype.updateIntent)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.ConversationV1.prototype.</span>updateWorkspace (params, callback)](#apidoc.element.watson-developer-cloud.ConversationV1.prototype.updateWorkspace)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.ConversationV1.prototype.</span>workspaceStatus (params, callback)](#apidoc.element.watson-developer-cloud.ConversationV1.prototype.workspaceStatus)
1.  string <span class="apidocSignatureSpan">watson-developer-cloud.ConversationV1.prototype.</span>name
1.  string <span class="apidocSignatureSpan">watson-developer-cloud.ConversationV1.prototype.</span>version

#### [module watson-developer-cloud.ConversationV1Experimental](#apidoc.module.watson-developer-cloud.ConversationV1Experimental)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.</span>ConversationV1Experimental (options)](#apidoc.element.watson-developer-cloud.ConversationV1Experimental.ConversationV1Experimental)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.ConversationV1Experimental.</span>super_ (user_options)](#apidoc.element.watson-developer-cloud.ConversationV1Experimental.super_)
1.  string <span class="apidocSignatureSpan">watson-developer-cloud.ConversationV1Experimental.</span>URL

#### [module watson-developer-cloud.ConversationV1Experimental.prototype](#apidoc.module.watson-developer-cloud.ConversationV1Experimental.prototype)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.ConversationV1Experimental.prototype.</span>message (params, callback)](#apidoc.element.watson-developer-cloud.ConversationV1Experimental.prototype.message)
1.  string <span class="apidocSignatureSpan">watson-developer-cloud.ConversationV1Experimental.prototype.</span>name
1.  string <span class="apidocSignatureSpan">watson-developer-cloud.ConversationV1Experimental.prototype.</span>version

#### [module watson-developer-cloud.DialogV1](#apidoc.module.watson-developer-cloud.DialogV1)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.</span>DialogV1 (options)](#apidoc.element.watson-developer-cloud.DialogV1.DialogV1)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.DialogV1.</span>super_ (user_options)](#apidoc.element.watson-developer-cloud.DialogV1.super_)
1.  string <span class="apidocSignatureSpan">watson-developer-cloud.DialogV1.</span>URL

#### [module watson-developer-cloud.DialogV1.prototype](#apidoc.module.watson-developer-cloud.DialogV1.prototype)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.DialogV1.prototype.</span>conversation (params, callback)](#apidoc.element.watson-developer-cloud.DialogV1.prototype.conversation)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.DialogV1.prototype.</span>createDialog (params, callback)](#apidoc.element.watson-developer-cloud.DialogV1.prototype.createDialog)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.DialogV1.prototype.</span>deleteDialog (params, callback)](#apidoc.element.watson-developer-cloud.DialogV1.prototype.deleteDialog)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.DialogV1.prototype.</span>getContent (params, callback)](#apidoc.element.watson-developer-cloud.DialogV1.prototype.getContent)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.DialogV1.prototype.</span>getConversation (params, callback)](#apidoc.element.watson-developer-cloud.DialogV1.prototype.getConversation)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.DialogV1.prototype.</span>getDialogs (params, callback)](#apidoc.element.watson-developer-cloud.DialogV1.prototype.getDialogs)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.DialogV1.prototype.</span>getProfile (params, callback)](#apidoc.element.watson-developer-cloud.DialogV1.prototype.getProfile)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.DialogV1.prototype.</span>updateContent (params, callback)](#apidoc.element.watson-developer-cloud.DialogV1.prototype.updateContent)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.DialogV1.prototype.</span>updateDialog (params, callback)](#apidoc.element.watson-developer-cloud.DialogV1.prototype.updateDialog)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.DialogV1.prototype.</span>updateProfile (params, callback)](#apidoc.element.watson-developer-cloud.DialogV1.prototype.updateProfile)
1.  string <span class="apidocSignatureSpan">watson-developer-cloud.DialogV1.prototype.</span>name
1.  string <span class="apidocSignatureSpan">watson-developer-cloud.DialogV1.prototype.</span>version

#### [module watson-developer-cloud.DiscoveryV1](#apidoc.module.watson-developer-cloud.DiscoveryV1)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.</span>DiscoveryV1 (options)](#apidoc.element.watson-developer-cloud.DiscoveryV1.DiscoveryV1)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.DiscoveryV1.</span>super_ (user_options)](#apidoc.element.watson-developer-cloud.DiscoveryV1.super_)
1.  string <span class="apidocSignatureSpan">watson-developer-cloud.DiscoveryV1.</span>URL
1.  string <span class="apidocSignatureSpan">watson-developer-cloud.DiscoveryV1.</span>VERSION_DATE_2016_12_15

#### [module watson-developer-cloud.DiscoveryV1.prototype](#apidoc.module.watson-developer-cloud.DiscoveryV1.prototype)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.DiscoveryV1.prototype.</span>addDocument (params, callback)](#apidoc.element.watson-developer-cloud.DiscoveryV1.prototype.addDocument)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.DiscoveryV1.prototype.</span>createCollection (params, callback)](#apidoc.element.watson-developer-cloud.DiscoveryV1.prototype.createCollection)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.DiscoveryV1.prototype.</span>createEnvironment (params, callback)](#apidoc.element.watson-developer-cloud.DiscoveryV1.prototype.createEnvironment)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.DiscoveryV1.prototype.</span>deleteCollection (params, callback)](#apidoc.element.watson-developer-cloud.DiscoveryV1.prototype.deleteCollection)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.DiscoveryV1.prototype.</span>deleteDocument (params, callback)](#apidoc.element.watson-developer-cloud.DiscoveryV1.prototype.deleteDocument)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.DiscoveryV1.prototype.</span>deleteEnvironment (params, callback)](#apidoc.element.watson-developer-cloud.DiscoveryV1.prototype.deleteEnvironment)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.DiscoveryV1.prototype.</span>getCollection (params, callback)](#apidoc.element.watson-developer-cloud.DiscoveryV1.prototype.getCollection)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.DiscoveryV1.prototype.</span>getCollections (params, callback)](#apidoc.element.watson-developer-cloud.DiscoveryV1.prototype.getCollections)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.DiscoveryV1.prototype.</span>getConfiguration (params, callback)](#apidoc.element.watson-developer-cloud.DiscoveryV1.prototype.getConfiguration)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.DiscoveryV1.prototype.</span>getConfigurations (params, callback)](#apidoc.element.watson-developer-cloud.DiscoveryV1.prototype.getConfigurations)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.DiscoveryV1.prototype.</span>getEnvironment (params, callback)](#apidoc.element.watson-developer-cloud.DiscoveryV1.prototype.getEnvironment)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.DiscoveryV1.prototype.</span>getEnvironments (params, callback)](#apidoc.element.watson-developer-cloud.DiscoveryV1.prototype.getEnvironments)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.DiscoveryV1.prototype.</span>query (params, callback)](#apidoc.element.watson-developer-cloud.DiscoveryV1.prototype.query)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.DiscoveryV1.prototype.</span>updateDocument (params, callback)](#apidoc.element.watson-developer-cloud.DiscoveryV1.prototype.updateDocument)
1.  string <span class="apidocSignatureSpan">watson-developer-cloud.DiscoveryV1.prototype.</span>name
1.  string <span class="apidocSignatureSpan">watson-developer-cloud.DiscoveryV1.prototype.</span>version

#### [module watson-developer-cloud.DiscoveryV1Experimental](#apidoc.module.watson-developer-cloud.DiscoveryV1Experimental)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.</span>DiscoveryV1Experimental (options)](#apidoc.element.watson-developer-cloud.DiscoveryV1Experimental.DiscoveryV1Experimental)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.DiscoveryV1Experimental.</span>super_ (user_options)](#apidoc.element.watson-developer-cloud.DiscoveryV1Experimental.super_)
1.  string <span class="apidocSignatureSpan">watson-developer-cloud.DiscoveryV1Experimental.</span>URL
1.  string <span class="apidocSignatureSpan">watson-developer-cloud.DiscoveryV1Experimental.</span>VERSION_DATE_2016_07_11

#### [module watson-developer-cloud.DiscoveryV1Experimental.prototype](#apidoc.module.watson-developer-cloud.DiscoveryV1Experimental.prototype)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.DiscoveryV1Experimental.prototype.</span>getCollection (params, collectionId, callback)](#apidoc.element.watson-developer-cloud.DiscoveryV1Experimental.prototype.getCollection)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.DiscoveryV1Experimental.prototype.</span>getCollections (params, callback)](#apidoc.element.watson-developer-cloud.DiscoveryV1Experimental.prototype.getCollections)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.DiscoveryV1Experimental.prototype.</span>getEnvironment (params, callback)](#apidoc.element.watson-developer-cloud.DiscoveryV1Experimental.prototype.getEnvironment)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.DiscoveryV1Experimental.prototype.</span>getEnvironments (params, callback)](#apidoc.element.watson-developer-cloud.DiscoveryV1Experimental.prototype.getEnvironments)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.DiscoveryV1Experimental.prototype.</span>query (params, callback)](#apidoc.element.watson-developer-cloud.DiscoveryV1Experimental.prototype.query)
1.  string <span class="apidocSignatureSpan">watson-developer-cloud.DiscoveryV1Experimental.prototype.</span>name
1.  string <span class="apidocSignatureSpan">watson-developer-cloud.DiscoveryV1Experimental.prototype.</span>version

#### [module watson-developer-cloud.DocumentConversionV1](#apidoc.module.watson-developer-cloud.DocumentConversionV1)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.</span>DocumentConversionV1 (options)](#apidoc.element.watson-developer-cloud.DocumentConversionV1.DocumentConversionV1)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.DocumentConversionV1.</span>super_ (user_options)](#apidoc.element.watson-developer-cloud.DocumentConversionV1.super_)
1.  string <span class="apidocSignatureSpan">watson-developer-cloud.DocumentConversionV1.</span>URL

#### [module watson-developer-cloud.DocumentConversionV1.prototype](#apidoc.module.watson-developer-cloud.DocumentConversionV1.prototype)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.DocumentConversionV1.prototype.</span>addDocumentToBatch ()](#apidoc.element.watson-developer-cloud.DocumentConversionV1.prototype.addDocumentToBatch)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.DocumentConversionV1.prototype.</span>convert (params, callback)](#apidoc.element.watson-developer-cloud.DocumentConversionV1.prototype.convert)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.DocumentConversionV1.prototype.</span>createBatch ()](#apidoc.element.watson-developer-cloud.DocumentConversionV1.prototype.createBatch)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.DocumentConversionV1.prototype.</span>createJob ()](#apidoc.element.watson-developer-cloud.DocumentConversionV1.prototype.createJob)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.DocumentConversionV1.prototype.</span>getBatch ()](#apidoc.element.watson-developer-cloud.DocumentConversionV1.prototype.getBatch)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.DocumentConversionV1.prototype.</span>getBatchDocument ()](#apidoc.element.watson-developer-cloud.DocumentConversionV1.prototype.getBatchDocument)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.DocumentConversionV1.prototype.</span>getBatchDocuments ()](#apidoc.element.watson-developer-cloud.DocumentConversionV1.prototype.getBatchDocuments)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.DocumentConversionV1.prototype.</span>getBatches ()](#apidoc.element.watson-developer-cloud.DocumentConversionV1.prototype.getBatches)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.DocumentConversionV1.prototype.</span>getDocument ()](#apidoc.element.watson-developer-cloud.DocumentConversionV1.prototype.getDocument)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.DocumentConversionV1.prototype.</span>getDocuments ()](#apidoc.element.watson-developer-cloud.DocumentConversionV1.prototype.getDocuments)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.DocumentConversionV1.prototype.</span>getJob ()](#apidoc.element.watson-developer-cloud.DocumentConversionV1.prototype.getJob)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.DocumentConversionV1.prototype.</span>getJobLog ()](#apidoc.element.watson-developer-cloud.DocumentConversionV1.prototype.getJobLog)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.DocumentConversionV1.prototype.</span>getJobs ()](#apidoc.element.watson-developer-cloud.DocumentConversionV1.prototype.getJobs)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.DocumentConversionV1.prototype.</span>getOutput ()](#apidoc.element.watson-developer-cloud.DocumentConversionV1.prototype.getOutput)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.DocumentConversionV1.prototype.</span>getOutputs ()](#apidoc.element.watson-developer-cloud.DocumentConversionV1.prototype.getOutputs)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.DocumentConversionV1.prototype.</span>index (params, callback)](#apidoc.element.watson-developer-cloud.DocumentConversionV1.prototype.index)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.DocumentConversionV1.prototype.</span>updateBatch ()](#apidoc.element.watson-developer-cloud.DocumentConversionV1.prototype.updateBatch)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.DocumentConversionV1.prototype.</span>uploadDocument ()](#apidoc.element.watson-developer-cloud.DocumentConversionV1.prototype.uploadDocument)
1.  object <span class="apidocSignatureSpan">watson-developer-cloud.DocumentConversionV1.prototype.</span>conversion_target
1.  object <span class="apidocSignatureSpan">watson-developer-cloud.DocumentConversionV1.prototype.</span>serviceDefaults
1.  string <span class="apidocSignatureSpan">watson-developer-cloud.DocumentConversionV1.prototype.</span>name
1.  string <span class="apidocSignatureSpan">watson-developer-cloud.DocumentConversionV1.prototype.</span>version

#### [module watson-developer-cloud.LanguageTranslationV2](#apidoc.module.watson-developer-cloud.LanguageTranslationV2)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.</span>LanguageTranslationV2 (options)](#apidoc.element.watson-developer-cloud.LanguageTranslationV2.LanguageTranslationV2)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.LanguageTranslationV2.</span>super_ (user_options)](#apidoc.element.watson-developer-cloud.LanguageTranslationV2.super_)
1.  string <span class="apidocSignatureSpan">watson-developer-cloud.LanguageTranslationV2.</span>URL

#### [module watson-developer-cloud.LanguageTranslationV2.prototype](#apidoc.module.watson-developer-cloud.LanguageTranslationV2.prototype)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.LanguageTranslationV2.prototype.</span>createModel (params, callback)](#apidoc.element.watson-developer-cloud.LanguageTranslationV2.prototype.createModel)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.LanguageTranslationV2.prototype.</span>deleteModel (params, callback)](#apidoc.element.watson-developer-cloud.LanguageTranslationV2.prototype.deleteModel)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.LanguageTranslationV2.prototype.</span>getIdentifiableLanguages (params, callback)](#apidoc.element.watson-developer-cloud.LanguageTranslationV2.prototype.getIdentifiableLanguages)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.LanguageTranslationV2.prototype.</span>getModel (params, callback)](#apidoc.element.watson-developer-cloud.LanguageTranslationV2.prototype.getModel)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.LanguageTranslationV2.prototype.</span>getModels (params, callback)](#apidoc.element.watson-developer-cloud.LanguageTranslationV2.prototype.getModels)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.LanguageTranslationV2.prototype.</span>identify (params, callback)](#apidoc.element.watson-developer-cloud.LanguageTranslationV2.prototype.identify)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.LanguageTranslationV2.prototype.</span>translate (params, callback)](#apidoc.element.watson-developer-cloud.LanguageTranslationV2.prototype.translate)
1.  string <span class="apidocSignatureSpan">watson-developer-cloud.LanguageTranslationV2.prototype.</span>name
1.  string <span class="apidocSignatureSpan">watson-developer-cloud.LanguageTranslationV2.prototype.</span>version

#### [module watson-developer-cloud.LanguageTranslatorV2](#apidoc.module.watson-developer-cloud.LanguageTranslatorV2)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.</span>LanguageTranslatorV2 (options)](#apidoc.element.watson-developer-cloud.LanguageTranslatorV2.LanguageTranslatorV2)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.LanguageTranslatorV2.</span>super_ (user_options)](#apidoc.element.watson-developer-cloud.LanguageTranslatorV2.super_)
1.  string <span class="apidocSignatureSpan">watson-developer-cloud.LanguageTranslatorV2.</span>URL

#### [module watson-developer-cloud.LanguageTranslatorV2.prototype](#apidoc.module.watson-developer-cloud.LanguageTranslatorV2.prototype)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.LanguageTranslatorV2.prototype.</span>createModel (params, callback)](#apidoc.element.watson-developer-cloud.LanguageTranslatorV2.prototype.createModel)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.LanguageTranslatorV2.prototype.</span>deleteModel (params, callback)](#apidoc.element.watson-developer-cloud.LanguageTranslatorV2.prototype.deleteModel)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.LanguageTranslatorV2.prototype.</span>getIdentifiableLanguages (params, callback)](#apidoc.element.watson-developer-cloud.LanguageTranslatorV2.prototype.getIdentifiableLanguages)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.LanguageTranslatorV2.prototype.</span>getModel (params, callback)](#apidoc.element.watson-developer-cloud.LanguageTranslatorV2.prototype.getModel)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.LanguageTranslatorV2.prototype.</span>getModels (params, callback)](#apidoc.element.watson-developer-cloud.LanguageTranslatorV2.prototype.getModels)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.LanguageTranslatorV2.prototype.</span>identify (params, callback)](#apidoc.element.watson-developer-cloud.LanguageTranslatorV2.prototype.identify)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.LanguageTranslatorV2.prototype.</span>translate (params, callback)](#apidoc.element.watson-developer-cloud.LanguageTranslatorV2.prototype.translate)
1.  string <span class="apidocSignatureSpan">watson-developer-cloud.LanguageTranslatorV2.prototype.</span>name
1.  string <span class="apidocSignatureSpan">watson-developer-cloud.LanguageTranslatorV2.prototype.</span>version

#### [module watson-developer-cloud.NaturalLanguageClassifierV1](#apidoc.module.watson-developer-cloud.NaturalLanguageClassifierV1)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.</span>NaturalLanguageClassifierV1 (options)](#apidoc.element.watson-developer-cloud.NaturalLanguageClassifierV1.NaturalLanguageClassifierV1)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.NaturalLanguageClassifierV1.</span>super_ (user_options)](#apidoc.element.watson-developer-cloud.NaturalLanguageClassifierV1.super_)
1.  string <span class="apidocSignatureSpan">watson-developer-cloud.NaturalLanguageClassifierV1.</span>URL

#### [module watson-developer-cloud.NaturalLanguageClassifierV1.prototype](#apidoc.module.watson-developer-cloud.NaturalLanguageClassifierV1.prototype)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.NaturalLanguageClassifierV1.prototype.</span>classify (params, callback)](#apidoc.element.watson-developer-cloud.NaturalLanguageClassifierV1.prototype.classify)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.NaturalLanguageClassifierV1.prototype.</span>create (params, callback)](#apidoc.element.watson-developer-cloud.NaturalLanguageClassifierV1.prototype.create)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.NaturalLanguageClassifierV1.prototype.</span>list (params, callback)](#apidoc.element.watson-developer-cloud.NaturalLanguageClassifierV1.prototype.list)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.NaturalLanguageClassifierV1.prototype.</span>remove (params, callback)](#apidoc.element.watson-developer-cloud.NaturalLanguageClassifierV1.prototype.remove)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.NaturalLanguageClassifierV1.prototype.</span>status (params, callback)](#apidoc.element.watson-developer-cloud.NaturalLanguageClassifierV1.prototype.status)
1.  string <span class="apidocSignatureSpan">watson-developer-cloud.NaturalLanguageClassifierV1.prototype.</span>name
1.  string <span class="apidocSignatureSpan">watson-developer-cloud.NaturalLanguageClassifierV1.prototype.</span>version

#### [module watson-developer-cloud.NaturalLanguageUnderstandingV1](#apidoc.module.watson-developer-cloud.NaturalLanguageUnderstandingV1)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.</span>NaturalLanguageUnderstandingV1 (options)](#apidoc.element.watson-developer-cloud.NaturalLanguageUnderstandingV1.NaturalLanguageUnderstandingV1)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.NaturalLanguageUnderstandingV1.</span>super_ (user_options)](#apidoc.element.watson-developer-cloud.NaturalLanguageUnderstandingV1.super_)
1.  string <span class="apidocSignatureSpan">watson-developer-cloud.NaturalLanguageUnderstandingV1.</span>URL
1.  string <span class="apidocSignatureSpan">watson-developer-cloud.NaturalLanguageUnderstandingV1.</span>VERSION_DATE_2016_01_23
1.  string <span class="apidocSignatureSpan">watson-developer-cloud.NaturalLanguageUnderstandingV1.</span>VERSION_DATE_2017_02_27

#### [module watson-developer-cloud.NaturalLanguageUnderstandingV1.prototype](#apidoc.module.watson-developer-cloud.NaturalLanguageUnderstandingV1.prototype)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.NaturalLanguageUnderstandingV1.prototype.</span>analyze (params, callback)](#apidoc.element.watson-developer-cloud.NaturalLanguageUnderstandingV1.prototype.analyze)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.NaturalLanguageUnderstandingV1.prototype.</span>deleteModel (params, callback)](#apidoc.element.watson-developer-cloud.NaturalLanguageUnderstandingV1.prototype.deleteModel)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.NaturalLanguageUnderstandingV1.prototype.</span>getCredentialsFromBluemix (name)](#apidoc.element.watson-developer-cloud.NaturalLanguageUnderstandingV1.prototype.getCredentialsFromBluemix)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.NaturalLanguageUnderstandingV1.prototype.</span>listModels (params, callback)](#apidoc.element.watson-developer-cloud.NaturalLanguageUnderstandingV1.prototype.listModels)
1.  string <span class="apidocSignatureSpan">watson-developer-cloud.NaturalLanguageUnderstandingV1.prototype.</span>name
1.  string <span class="apidocSignatureSpan">watson-developer-cloud.NaturalLanguageUnderstandingV1.prototype.</span>version

#### [module watson-developer-cloud.PersonalityInsightsV2](#apidoc.module.watson-developer-cloud.PersonalityInsightsV2)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.</span>PersonalityInsightsV2 (options)](#apidoc.element.watson-developer-cloud.PersonalityInsightsV2.PersonalityInsightsV2)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.PersonalityInsightsV2.</span>super_ (user_options)](#apidoc.element.watson-developer-cloud.PersonalityInsightsV2.super_)
1.  string <span class="apidocSignatureSpan">watson-developer-cloud.PersonalityInsightsV2.</span>URL

#### [module watson-developer-cloud.PersonalityInsightsV2.prototype](#apidoc.module.watson-developer-cloud.PersonalityInsightsV2.prototype)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.PersonalityInsightsV2.prototype.</span>profile ( params, callback // eslint-disable-line complexity )](#apidoc.element.watson-developer-cloud.PersonalityInsightsV2.prototype.profile)
1.  string <span class="apidocSignatureSpan">watson-developer-cloud.PersonalityInsightsV2.prototype.</span>name
1.  string <span class="apidocSignatureSpan">watson-developer-cloud.PersonalityInsightsV2.prototype.</span>version

#### [module watson-developer-cloud.PersonalityInsightsV3](#apidoc.module.watson-developer-cloud.PersonalityInsightsV3)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.</span>PersonalityInsightsV3 (options)](#apidoc.element.watson-developer-cloud.PersonalityInsightsV3.PersonalityInsightsV3)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.PersonalityInsightsV3.</span>super_ (user_options)](#apidoc.element.watson-developer-cloud.PersonalityInsightsV3.super_)
1.  string <span class="apidocSignatureSpan">watson-developer-cloud.PersonalityInsightsV3.</span>URL

#### [module watson-developer-cloud.PersonalityInsightsV3.prototype](#apidoc.module.watson-developer-cloud.PersonalityInsightsV3.prototype)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.PersonalityInsightsV3.prototype.</span>profile ( _params, callback // eslint-disable-line complexity )](#apidoc.element.watson-developer-cloud.PersonalityInsightsV3.prototype.profile)
1.  string <span class="apidocSignatureSpan">watson-developer-cloud.PersonalityInsightsV3.prototype.</span>name
1.  string <span class="apidocSignatureSpan">watson-developer-cloud.PersonalityInsightsV3.prototype.</span>version

#### [module watson-developer-cloud.RetrieveAndRankV1](#apidoc.module.watson-developer-cloud.RetrieveAndRankV1)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.</span>RetrieveAndRankV1 (options)](#apidoc.element.watson-developer-cloud.RetrieveAndRankV1.RetrieveAndRankV1)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.RetrieveAndRankV1.</span>super_ (user_options)](#apidoc.element.watson-developer-cloud.RetrieveAndRankV1.super_)
1.  string <span class="apidocSignatureSpan">watson-developer-cloud.RetrieveAndRankV1.</span>URL

#### [module watson-developer-cloud.RetrieveAndRankV1.prototype](#apidoc.module.watson-developer-cloud.RetrieveAndRankV1.prototype)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.RetrieveAndRankV1.prototype.</span>createCluster (params, callback)](#apidoc.element.watson-developer-cloud.RetrieveAndRankV1.prototype.createCluster)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.RetrieveAndRankV1.prototype.</span>createCollection (params, callback)](#apidoc.element.watson-developer-cloud.RetrieveAndRankV1.prototype.createCollection)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.RetrieveAndRankV1.prototype.</span>createRanker (params, callback)](#apidoc.element.watson-developer-cloud.RetrieveAndRankV1.prototype.createRanker)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.RetrieveAndRankV1.prototype.</span>createSolrClient (params)](#apidoc.element.watson-developer-cloud.RetrieveAndRankV1.prototype.createSolrClient)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.RetrieveAndRankV1.prototype.</span>deleteCluster (params, callback)](#apidoc.element.watson-developer-cloud.RetrieveAndRankV1.prototype.deleteCluster)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.RetrieveAndRankV1.prototype.</span>deleteCollection (params, callback)](#apidoc.element.watson-developer-cloud.RetrieveAndRankV1.prototype.deleteCollection)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.RetrieveAndRankV1.prototype.</span>deleteConfig (params, callback)](#apidoc.element.watson-developer-cloud.RetrieveAndRankV1.prototype.deleteConfig)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.RetrieveAndRankV1.prototype.</span>deleteRanker (params, callback)](#apidoc.element.watson-developer-cloud.RetrieveAndRankV1.prototype.deleteRanker)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.RetrieveAndRankV1.prototype.</span>getClusterStats (params, callback)](#apidoc.element.watson-developer-cloud.RetrieveAndRankV1.prototype.getClusterStats)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.RetrieveAndRankV1.prototype.</span>getConfig (params, callback)](#apidoc.element.watson-developer-cloud.RetrieveAndRankV1.prototype.getConfig)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.RetrieveAndRankV1.prototype.</span>getResizeStatus (params, callback)](#apidoc.element.watson-developer-cloud.RetrieveAndRankV1.prototype.getResizeStatus)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.RetrieveAndRankV1.prototype.</span>listClusters (params, callback)](#apidoc.element.watson-developer-cloud.RetrieveAndRankV1.prototype.listClusters)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.RetrieveAndRankV1.prototype.</span>listCollections (params, callback)](#apidoc.element.watson-developer-cloud.RetrieveAndRankV1.prototype.listCollections)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.RetrieveAndRankV1.prototype.</span>listConfigs (params, callback)](#apidoc.element.watson-developer-cloud.RetrieveAndRankV1.prototype.listConfigs)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.RetrieveAndRankV1.prototype.</span>listRankers (params, callback)](#apidoc.element.watson-developer-cloud.RetrieveAndRankV1.prototype.listRankers)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.RetrieveAndRankV1.prototype.</span>pollCluster (params, callback)](#apidoc.element.watson-developer-cloud.RetrieveAndRankV1.prototype.pollCluster)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.RetrieveAndRankV1.prototype.</span>rank (params, callback)](#apidoc.element.watson-developer-cloud.RetrieveAndRankV1.prototype.rank)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.RetrieveAndRankV1.prototype.</span>rankerStatus (params, callback)](#apidoc.element.watson-developer-cloud.RetrieveAndRankV1.prototype.rankerStatus)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.RetrieveAndRankV1.prototype.</span>resizeCluster (params, callback)](#apidoc.element.watson-developer-cloud.RetrieveAndRankV1.prototype.resizeCluster)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.RetrieveAndRankV1.prototype.</span>uploadConfig (params, callback)](#apidoc.element.watson-developer-cloud.RetrieveAndRankV1.prototype.uploadConfig)
1.  string <span class="apidocSignatureSpan">watson-developer-cloud.RetrieveAndRankV1.prototype.</span>name
1.  string <span class="apidocSignatureSpan">watson-developer-cloud.RetrieveAndRankV1.prototype.</span>version

#### [module watson-developer-cloud.SpeechToTextV1](#apidoc.module.watson-developer-cloud.SpeechToTextV1)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.</span>SpeechToTextV1 (options)](#apidoc.element.watson-developer-cloud.SpeechToTextV1.SpeechToTextV1)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.SpeechToTextV1.</span>super_ (user_options)](#apidoc.element.watson-developer-cloud.SpeechToTextV1.super_)
1.  string <span class="apidocSignatureSpan">watson-developer-cloud.SpeechToTextV1.</span>ERR_NO_CORPORA
1.  string <span class="apidocSignatureSpan">watson-developer-cloud.SpeechToTextV1.</span>ERR_TIMEOUT
1.  string <span class="apidocSignatureSpan">watson-developer-cloud.SpeechToTextV1.</span>URL

#### [module watson-developer-cloud.SpeechToTextV1.prototype](#apidoc.module.watson-developer-cloud.SpeechToTextV1.prototype)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.SpeechToTextV1.prototype.</span>addCorpus (params, callback)](#apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.addCorpus)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.SpeechToTextV1.prototype.</span>addWord (params, callback)](#apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.addWord)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.SpeechToTextV1.prototype.</span>addWords (params, callback)](#apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.addWords)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.SpeechToTextV1.prototype.</span>createCustomization (params, callback)](#apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.createCustomization)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.SpeechToTextV1.prototype.</span>createRecognitionJob (params, callback)](#apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.createRecognitionJob)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.SpeechToTextV1.prototype.</span>createRecognizeStream (params)](#apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.createRecognizeStream)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.SpeechToTextV1.prototype.</span>createSession (params, callback)](#apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.createSession)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.SpeechToTextV1.prototype.</span>deleteCorpus (params, callback)](#apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.deleteCorpus)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.SpeechToTextV1.prototype.</span>deleteCustomization (params, callback)](#apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.deleteCustomization)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.SpeechToTextV1.prototype.</span>deleteRecognitionJob (params, callback)](#apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.deleteRecognitionJob)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.SpeechToTextV1.prototype.</span>deleteSession (params, callback)](#apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.deleteSession)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.SpeechToTextV1.prototype.</span>deleteWord (params, callback)](#apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.deleteWord)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.SpeechToTextV1.prototype.</span>getCorpora (params, callback)](#apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.getCorpora)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.SpeechToTextV1.prototype.</span>getCorpus (params, callback)](#apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.getCorpus)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.SpeechToTextV1.prototype.</span>getCustomization (params, callback)](#apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.getCustomization)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.SpeechToTextV1.prototype.</span>getCustomizations (params, callback)](#apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.getCustomizations)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.SpeechToTextV1.prototype.</span>getModel (params, callback)](#apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.getModel)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.SpeechToTextV1.prototype.</span>getModels (params, callback)](#apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.getModels)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.SpeechToTextV1.prototype.</span>getRecognitionJob (params, callback)](#apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.getRecognitionJob)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.SpeechToTextV1.prototype.</span>getRecognitionJobs (params, callback)](#apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.getRecognitionJobs)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.SpeechToTextV1.prototype.</span>getRecognizeStatus (params, callback)](#apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.getRecognizeStatus)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.SpeechToTextV1.prototype.</span>getWord (params, callback)](#apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.getWord)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.SpeechToTextV1.prototype.</span>getWords (params, callback)](#apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.getWords)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.SpeechToTextV1.prototype.</span>observeResult (params)](#apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.observeResult)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.SpeechToTextV1.prototype.</span>recognize (params, callback)](#apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.recognize)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.SpeechToTextV1.prototype.</span>recognizeLive (params)](#apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.recognizeLive)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.SpeechToTextV1.prototype.</span>registerCallback (params, callback)](#apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.registerCallback)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.SpeechToTextV1.prototype.</span>resetCustomization (params, callback)](#apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.resetCustomization)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.SpeechToTextV1.prototype.</span>trainCustomization (params, callback)](#apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.trainCustomization)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.SpeechToTextV1.prototype.</span>whenCorporaAnalyzed (params, callback)](#apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.whenCorporaAnalyzed)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.SpeechToTextV1.prototype.</span>whenCustomizationReady (params, callback)](#apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.whenCustomizationReady)
1.  string <span class="apidocSignatureSpan">watson-developer-cloud.SpeechToTextV1.prototype.</span>name
1.  string <span class="apidocSignatureSpan">watson-developer-cloud.SpeechToTextV1.prototype.</span>version

#### [module watson-developer-cloud.TextToSpeechV1](#apidoc.module.watson-developer-cloud.TextToSpeechV1)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.</span>TextToSpeechV1 (options)](#apidoc.element.watson-developer-cloud.TextToSpeechV1.TextToSpeechV1)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.TextToSpeechV1.</span>super_ (user_options)](#apidoc.element.watson-developer-cloud.TextToSpeechV1.super_)
1.  string <span class="apidocSignatureSpan">watson-developer-cloud.TextToSpeechV1.</span>URL

#### [module watson-developer-cloud.TextToSpeechV1.prototype](#apidoc.module.watson-developer-cloud.TextToSpeechV1.prototype)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.TextToSpeechV1.prototype.</span>addWord (params, callback)](#apidoc.element.watson-developer-cloud.TextToSpeechV1.prototype.addWord)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.TextToSpeechV1.prototype.</span>addWords (params, callback)](#apidoc.element.watson-developer-cloud.TextToSpeechV1.prototype.addWords)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.TextToSpeechV1.prototype.</span>createCustomization (params, callback)](#apidoc.element.watson-developer-cloud.TextToSpeechV1.prototype.createCustomization)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.TextToSpeechV1.prototype.</span>deleteCustomization (params, callback)](#apidoc.element.watson-developer-cloud.TextToSpeechV1.prototype.deleteCustomization)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.TextToSpeechV1.prototype.</span>deleteWord (params, callback)](#apidoc.element.watson-developer-cloud.TextToSpeechV1.prototype.deleteWord)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.TextToSpeechV1.prototype.</span>getCustomization (params, callback)](#apidoc.element.watson-developer-cloud.TextToSpeechV1.prototype.getCustomization)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.TextToSpeechV1.prototype.</span>getCustomizations (params, callback)](#apidoc.element.watson-developer-cloud.TextToSpeechV1.prototype.getCustomizations)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.TextToSpeechV1.prototype.</span>getWord (params, callback)](#apidoc.element.watson-developer-cloud.TextToSpeechV1.prototype.getWord)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.TextToSpeechV1.prototype.</span>getWords (params, callback)](#apidoc.element.watson-developer-cloud.TextToSpeechV1.prototype.getWords)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.TextToSpeechV1.prototype.</span>pronunciation (params, callback)](#apidoc.element.watson-developer-cloud.TextToSpeechV1.prototype.pronunciation)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.TextToSpeechV1.prototype.</span>synthesize (params, callback)](#apidoc.element.watson-developer-cloud.TextToSpeechV1.prototype.synthesize)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.TextToSpeechV1.prototype.</span>updateCustomization (params, callback)](#apidoc.element.watson-developer-cloud.TextToSpeechV1.prototype.updateCustomization)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.TextToSpeechV1.prototype.</span>voice (params, callback)](#apidoc.element.watson-developer-cloud.TextToSpeechV1.prototype.voice)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.TextToSpeechV1.prototype.</span>voices (params, callback)](#apidoc.element.watson-developer-cloud.TextToSpeechV1.prototype.voices)
1.  string <span class="apidocSignatureSpan">watson-developer-cloud.TextToSpeechV1.prototype.</span>name
1.  string <span class="apidocSignatureSpan">watson-developer-cloud.TextToSpeechV1.prototype.</span>version

#### [module watson-developer-cloud.ToneAnalyzerV3](#apidoc.module.watson-developer-cloud.ToneAnalyzerV3)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.</span>ToneAnalyzerV3 (options)](#apidoc.element.watson-developer-cloud.ToneAnalyzerV3.ToneAnalyzerV3)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.ToneAnalyzerV3.</span>super_ (user_options)](#apidoc.element.watson-developer-cloud.ToneAnalyzerV3.super_)
1.  string <span class="apidocSignatureSpan">watson-developer-cloud.ToneAnalyzerV3.</span>URL

#### [module watson-developer-cloud.ToneAnalyzerV3.prototype](#apidoc.module.watson-developer-cloud.ToneAnalyzerV3.prototype)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.ToneAnalyzerV3.prototype.</span>tone (params, callback)](#apidoc.element.watson-developer-cloud.ToneAnalyzerV3.prototype.tone)
1.  string <span class="apidocSignatureSpan">watson-developer-cloud.ToneAnalyzerV3.prototype.</span>name
1.  string <span class="apidocSignatureSpan">watson-developer-cloud.ToneAnalyzerV3.prototype.</span>version

#### [module watson-developer-cloud.TradeoffAnalyticsV1](#apidoc.module.watson-developer-cloud.TradeoffAnalyticsV1)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.</span>TradeoffAnalyticsV1 (options)](#apidoc.element.watson-developer-cloud.TradeoffAnalyticsV1.TradeoffAnalyticsV1)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.TradeoffAnalyticsV1.</span>super_ (user_options)](#apidoc.element.watson-developer-cloud.TradeoffAnalyticsV1.super_)
1.  string <span class="apidocSignatureSpan">watson-developer-cloud.TradeoffAnalyticsV1.</span>URL

#### [module watson-developer-cloud.TradeoffAnalyticsV1.prototype](#apidoc.module.watson-developer-cloud.TradeoffAnalyticsV1.prototype)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.TradeoffAnalyticsV1.prototype.</span>dilemmas (params, callback)](#apidoc.element.watson-developer-cloud.TradeoffAnalyticsV1.prototype.dilemmas)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.TradeoffAnalyticsV1.prototype.</span>events (params, callback)](#apidoc.element.watson-developer-cloud.TradeoffAnalyticsV1.prototype.events)
1.  string <span class="apidocSignatureSpan">watson-developer-cloud.TradeoffAnalyticsV1.prototype.</span>name
1.  string <span class="apidocSignatureSpan">watson-developer-cloud.TradeoffAnalyticsV1.prototype.</span>version

#### [module watson-developer-cloud.VisualRecognitionV3](#apidoc.module.watson-developer-cloud.VisualRecognitionV3)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.</span>VisualRecognitionV3 (options)](#apidoc.element.watson-developer-cloud.VisualRecognitionV3.VisualRecognitionV3)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.VisualRecognitionV3.</span>super_ (user_options)](#apidoc.element.watson-developer-cloud.VisualRecognitionV3.super_)
1.  string <span class="apidocSignatureSpan">watson-developer-cloud.VisualRecognitionV3.</span>URL

#### [module watson-developer-cloud.VisualRecognitionV3.prototype](#apidoc.module.watson-developer-cloud.VisualRecognitionV3.prototype)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.VisualRecognitionV3.prototype.</span>addImage (params, callback)](#apidoc.element.watson-developer-cloud.VisualRecognitionV3.prototype.addImage)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.VisualRecognitionV3.prototype.</span>classify (params, callback)](#apidoc.element.watson-developer-cloud.VisualRecognitionV3.prototype.classify)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.VisualRecognitionV3.prototype.</span>createClassifier (params, callback)](#apidoc.element.watson-developer-cloud.VisualRecognitionV3.prototype.createClassifier)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.VisualRecognitionV3.prototype.</span>createCollection (params, callback)](#apidoc.element.watson-developer-cloud.VisualRecognitionV3.prototype.createCollection)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.VisualRecognitionV3.prototype.</span>deleteClassifier (params, callback)](#apidoc.element.watson-developer-cloud.VisualRecognitionV3.prototype.deleteClassifier)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.VisualRecognitionV3.prototype.</span>deleteCollection (params, callback)](#apidoc.element.watson-developer-cloud.VisualRecognitionV3.prototype.deleteCollection)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.VisualRecognitionV3.prototype.</span>deleteImage (params, callback)](#apidoc.element.watson-developer-cloud.VisualRecognitionV3.prototype.deleteImage)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.VisualRecognitionV3.prototype.</span>deleteImageMetadata (params, callback)](#apidoc.element.watson-developer-cloud.VisualRecognitionV3.prototype.deleteImageMetadata)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.VisualRecognitionV3.prototype.</span>detectFaces (params, callback)](#apidoc.element.watson-developer-cloud.VisualRecognitionV3.prototype.detectFaces)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.VisualRecognitionV3.prototype.</span>findSimilar (params, callback)](#apidoc.element.watson-developer-cloud.VisualRecognitionV3.prototype.findSimilar)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.VisualRecognitionV3.prototype.</span>getClassifier (params, callback)](#apidoc.element.watson-developer-cloud.VisualRecognitionV3.prototype.getClassifier)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.VisualRecognitionV3.prototype.</span>getCollection (params, callback)](#apidoc.element.watson-developer-cloud.VisualRecognitionV3.prototype.getCollection)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.VisualRecognitionV3.prototype.</span>getCredentialsFromBluemix ()](#apidoc.element.watson-developer-cloud.VisualRecognitionV3.prototype.getCredentialsFromBluemix)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.VisualRecognitionV3.prototype.</span>getCredentialsFromEnvironment (name)](#apidoc.element.watson-developer-cloud.VisualRecognitionV3.prototype.getCredentialsFromEnvironment)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.VisualRecognitionV3.prototype.</span>getImage (params, callback)](#apidoc.element.watson-developer-cloud.VisualRecognitionV3.prototype.getImage)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.VisualRecognitionV3.prototype.</span>getImageMetadata (params, callback)](#apidoc.element.watson-developer-cloud.VisualRecognitionV3.prototype.getImageMetadata)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.VisualRecognitionV3.prototype.</span>initCredentials (options)](#apidoc.element.watson-developer-cloud.VisualRecognitionV3.prototype.initCredentials)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.VisualRecognitionV3.prototype.</span>listClassifiers (params, callback)](#apidoc.element.watson-developer-cloud.VisualRecognitionV3.prototype.listClassifiers)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.VisualRecognitionV3.prototype.</span>listCollections (params, callback)](#apidoc.element.watson-developer-cloud.VisualRecognitionV3.prototype.listCollections)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.VisualRecognitionV3.prototype.</span>listImages (params, callback)](#apidoc.element.watson-developer-cloud.VisualRecognitionV3.prototype.listImages)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.VisualRecognitionV3.prototype.</span>recognizeText (params, callback)](#apidoc.element.watson-developer-cloud.VisualRecognitionV3.prototype.recognizeText)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.VisualRecognitionV3.prototype.</span>request (parameters, cb)](#apidoc.element.watson-developer-cloud.VisualRecognitionV3.prototype.request)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.VisualRecognitionV3.prototype.</span>retrainClassifier (params, callback)](#apidoc.element.watson-developer-cloud.VisualRecognitionV3.prototype.retrainClassifier)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.VisualRecognitionV3.prototype.</span>setImageMetadata (params, callback)](#apidoc.element.watson-developer-cloud.VisualRecognitionV3.prototype.setImageMetadata)
1.  object <span class="apidocSignatureSpan">watson-developer-cloud.VisualRecognitionV3.prototype.</span>serviceDefaults
1.  string <span class="apidocSignatureSpan">watson-developer-cloud.VisualRecognitionV3.prototype.</span>name
1.  string <span class="apidocSignatureSpan">watson-developer-cloud.VisualRecognitionV3.prototype.</span>version

#### [module watson-developer-cloud.helper](#apidoc.module.watson-developer-cloud.helper)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.helper.</span>getFormat (params, formats)](#apidoc.element.watson-developer-cloud.helper.getFormat)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.helper.</span>getMissingParams (params, requires)](#apidoc.element.watson-developer-cloud.helper.getMissingParams)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.helper.</span>isHTML (text)](#apidoc.element.watson-developer-cloud.helper.isHTML)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.helper.</span>stripTrailingSlash (url)](#apidoc.element.watson-developer-cloud.helper.stripTrailingSlash)

#### [module watson-developer-cloud.recognize_stream](#apidoc.module.watson-developer-cloud.recognize_stream)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.</span>recognize_stream (options)](#apidoc.element.watson-developer-cloud.recognize_stream.recognize_stream)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.recognize_stream.</span>getContentType (buffer)](#apidoc.element.watson-developer-cloud.recognize_stream.getContentType)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.recognize_stream.</span>super_ (options)](#apidoc.element.watson-developer-cloud.recognize_stream.super_)

#### [module watson-developer-cloud.recognize_stream.prototype](#apidoc.module.watson-developer-cloud.recognize_stream.prototype)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.recognize_stream.prototype.</span>_read ()](#apidoc.element.watson-developer-cloud.recognize_stream.prototype._read)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.recognize_stream.prototype.</span>_write (chunk, encoding, callback)](#apidoc.element.watson-developer-cloud.recognize_stream.prototype._write)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.recognize_stream.prototype.</span>afterSend (next)](#apidoc.element.watson-developer-cloud.recognize_stream.prototype.afterSend)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.recognize_stream.prototype.</span>getTransactionId ()](#apidoc.element.watson-developer-cloud.recognize_stream.prototype.getTransactionId)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.recognize_stream.prototype.</span>initialize ()](#apidoc.element.watson-developer-cloud.recognize_stream.prototype.initialize)
1.  [function <span class="apidocSignatureSpan">watson-developer-cloud.recognize_stream.prototype.</span>stop ()](#apidoc.element.watson-developer-cloud.recognize_stream.prototype.stop)



# <a name="apidoc.module.watson-developer-cloud"></a>[module watson-developer-cloud](#apidoc.module.watson-developer-cloud)

#### <a name="apidoc.element.watson-developer-cloud.AlchemyDataNewsV1"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.</span>AlchemyDataNewsV1 (options)](#apidoc.element.watson-developer-cloud.AlchemyDataNewsV1)
- description and source-code
```javascript
function AlchemyDataNewsV1(options) {
  BaseServiceAlchemy.call(this, options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.AlchemyDataNewsV1.super_"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.</span>AlchemyDataNewsV1.super_ (options)](#apidoc.element.watson-developer-cloud.AlchemyDataNewsV1.super_)
- description and source-code
```javascript
function BaseServiceAlchemy(options) {
  BaseService.call(this, options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.AlchemyLanguageV1"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.</span>AlchemyLanguageV1 (options)](#apidoc.element.watson-developer-cloud.AlchemyLanguageV1)
- description and source-code
```javascript
function AlchemyLanguageV1(options) {
  BaseServiceAlchemy.call(this, options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.AlchemyVisionV1"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.</span>AlchemyVisionV1 (options)](#apidoc.element.watson-developer-cloud.AlchemyVisionV1)
- description and source-code
```javascript
function AlchemyVisionV1(options) {
  BaseServiceAlchemy.call(this, options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.AuthorizationV1"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.</span>AuthorizationV1 (options)](#apidoc.element.watson-developer-cloud.AuthorizationV1)
- description and source-code
```javascript
function AuthorizationV1(options) {
  BaseService.call(this, options);
  this.target_url = options.url;
  // replace the url to always point to /authorization/api
  const hostname = url.parse(this._options.url);
  hostname.pathname = '/authorization/api';
  this._options.url = url.format(hostname);
}
```
- example usage
```shell
...
Tokens are valid for 1 hour and may be sent using the 'X-Watson-Authorization-Token' header or the 'watson-token' query param.

Note that the token is supplied URL-encoded, and will not be accepted if it is double-encoded in a querystring.

'''javascript
var watson = require('watson-developer-cloud');

var authorization = new watson.AuthorizationV1({
username: '<Text to Speech username>',
password: '<Text to Speech password>',
url: watson.TextToSpeechV1.URL
});

authorization.getToken(function (err, token) {
if (!token) {
...
```

#### <a name="apidoc.element.watson-developer-cloud.AuthorizationV1.super_"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.</span>AuthorizationV1.super_ (user_options)](#apidoc.element.watson-developer-cloud.AuthorizationV1.super_)
- description and source-code
```javascript
function BaseService(user_options) {
  if (!(this instanceof BaseService)) {
    // it might be better to just create a new instance and return that.. but that can't be done here, it has to be done in each
 individual service. So this is still a good failsafe even in that case.
    throw new Error('"new" keyword required to create Watson service instances');
  }
  let options = extend({}, user_options);

  options = this.initCredentials(options);

  if (options.url) {
    options.url = helper.stripTrailingSlash(options.url);
  }

  this._options = extend({ qs: {}, url: this.constructor.URL }, this.serviceDefaults, options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.ConversationV1"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.</span>ConversationV1 (options)](#apidoc.element.watson-developer-cloud.ConversationV1)
- description and source-code
```javascript
function ConversationV1(options) {
  BaseService.call(this, options);

  // Check if 'version_date' was provided
  if (typeof this._options.version_date === 'undefined') {
    throw new Error('Argument error: version_date was not specified, use ConversationV1.VERSION_DATE_2017_02_03');
  }
  this._options.qs.version = options.version_date;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.ConversationV1Experimental"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.</span>ConversationV1Experimental (options)](#apidoc.element.watson-developer-cloud.ConversationV1Experimental)
- description and source-code
```javascript
function ConversationV1Experimental(options) {
  BaseService.call(this, options);

  if (!this._options.silent) {
    // eslint-disable-next-line no-console
    console.warn(
      new Error('Watson Conversation v1-experimental is sunset as of 2016-08-01. Please upgrade to v1. Set {silent: true} to disable
 this message.').stack
    );
  }

  // Check if 'version_date' was provided
  if (typeof this._options.version_date === 'undefined') {
    throw new Error('Argument error: version_date was not specified, use 2016-05-19');
  }
  this._options.qs.version = options.version_date;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.DialogV1"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.</span>DialogV1 (options)](#apidoc.element.watson-developer-cloud.DialogV1)
- description and source-code
```javascript
function DialogV1(options) {
  BaseService.call(this, options);

  if (!options.silent) {
    // eslint-disable-next-line no-console
    console.warn(
      'WARNING: The Dialog service was deprecated, existing instances of the service will continue to function until August 9, 2017
. See https://www.ibm.com/watson/developercloud/doc/conversation/migration.shtml. Set {silent: true} to disable this message.'
    );
  }
}
```
- example usage
```shell
...
By default, the library tries to use Basic Auth and will ask for 'api_key' or 'username' and 'password' and send an 'Authorization
: Basic XXXXXXX'. You can avoid this by using:

'use_unauthenticated'.

'''javascript
var watson = require('watson-developer-cloud');

var dialog = new watson.DialogV1({
  use_unauthenticated: true
});
'''

## Debug
This library relies on the 'request' npm module writted by
[request][request_github] to call the Watson Services. To debug the apps, add
...
```

#### <a name="apidoc.element.watson-developer-cloud.DiscoveryV1"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.</span>DiscoveryV1 (options)](#apidoc.element.watson-developer-cloud.DiscoveryV1)
- description and source-code
```javascript
function DiscoveryV1(options) {
  BaseService.call(this, options);

  // Check if 'version_date' was provided
  if (typeof this._options.version_date === 'undefined') {
    throw new Error('Argument error: version_date was not specified, use DiscoveryV1.VERSION_DATE_2016_12_15');
  }
  this._options.qs.version = options.version_date;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.DiscoveryV1Experimental"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.</span>DiscoveryV1Experimental (options)](#apidoc.element.watson-developer-cloud.DiscoveryV1Experimental)
- description and source-code
```javascript
function DiscoveryV1Experimental(options) {
  BaseService.call(this, options);

  // Check if 'version_date' was provided
  if (typeof this._options.version_date === 'undefined') {
    throw new Error('Argument error: version_date was not specified, use DiscoveryV1Experimental.VERSION_DATE_2016_07_11');
  }
  this._options.qs.version = options.version_date;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.DocumentConversionV1"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.</span>DocumentConversionV1 (options)](#apidoc.element.watson-developer-cloud.DocumentConversionV1)
- description and source-code
```javascript
function DocumentConversionV1(options) {
  BaseService.call(this, options);

  // Warn if not specifying version date
  if (!this._options.version_date && !this._options.silent) {
    // eslint-disable-next-line no-console
    console.warn(
      '[DocumentConversion] WARNING: No version_date specified. Using a (possibly old) default. ' +
        'e.g. watson.document_conversion({ version_date: "2015-12-15" })'
    );
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.LanguageTranslationV2"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.</span>LanguageTranslationV2 (options)](#apidoc.element.watson-developer-cloud.LanguageTranslationV2)
- description and source-code
```javascript
function LanguageTranslationV2(options) {
  BaseService.call(this, options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.LanguageTranslatorV2"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.</span>LanguageTranslatorV2 (options)](#apidoc.element.watson-developer-cloud.LanguageTranslatorV2)
- description and source-code
```javascript
function LanguageTranslatorV2(options) {
  // Welp, this is awkward. Originally the rename was *just* a rename, but then (after the SDK was updated,
  // but before the backend was updated), it was decided that the billing should be simplified at the same time.
  // That's a solid improvement, but it means that the SDK now needs to support both services independently,
  // and correcting the default URL here will break older code, so it must be reserved for a major release.
  // todo: consider checking for options.url === LanguageTranslationV2.URL and also throw this warning then.
  // (This probably does't matter since the api didn't change)
  if (!options.url) {
    const err = new Error(
      'LanguageTranslatorV2 currently defaults to the url for LanguageTranslationV2, ' +
        'but this will change in the next major release of the watson-developer-cloud Node.js SDK. ' +
        'Please either specify the url https://gateway.watsonplatform.net/language-translator/api or else use ' +
        'LanguageTranslationV2. ' +
        'See http://www.ibm.com/watson/developercloud/doc/language-translator/migrating.shtml for more details.'
    );
    // eslint-disable-next-line no-console
    console.warn(err);
  }

  BaseService.call(this, options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.NaturalLanguageClassifierV1"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.</span>NaturalLanguageClassifierV1 (options)](#apidoc.element.watson-developer-cloud.NaturalLanguageClassifierV1)
- description and source-code
```javascript
function NaturalLanguageClassifierV1(options) {
  BaseService.call(this, options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.NaturalLanguageUnderstandingV1"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.</span>NaturalLanguageUnderstandingV1 (options)](#apidoc.element.watson-developer-cloud.NaturalLanguageUnderstandingV1)
- description and source-code
```javascript
function NaturalLanguageUnderstandingV1(options) {
  BaseService.call(this, options);
  if (typeof this._options.version_date === 'undefined') {
    throw new Error('Argument error: version_date was not specified, use NaturalLanguageUnderstandingV1.VERSION_DATE_2017_02_27');
  }
  this._options.qs.version = this._options.version_date;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.PersonalityInsightsV2"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.</span>PersonalityInsightsV2 (options)](#apidoc.element.watson-developer-cloud.PersonalityInsightsV2)
- description and source-code
```javascript
function PersonalityInsightsV2(options) {
  BaseService.call(this, options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.PersonalityInsightsV3"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.</span>PersonalityInsightsV3 (options)](#apidoc.element.watson-developer-cloud.PersonalityInsightsV3)
- description and source-code
```javascript
function PersonalityInsightsV3(options) {
  BaseService.call(this, options);

  // Check if 'version_date' was provided
  if (typeof this._options.version_date === 'undefined') {
    throw new Error('Argument error: version_date was not specified, use 2016-10-19');
  }
  this._options.qs.version = options.version_date;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.RetrieveAndRankV1"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.</span>RetrieveAndRankV1 (options)](#apidoc.element.watson-developer-cloud.RetrieveAndRankV1)
- description and source-code
```javascript
function RetrieveAndRankV1(options) {
  BaseService.call(this, options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.SpeechToTextV1"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.</span>SpeechToTextV1 (options)](#apidoc.element.watson-developer-cloud.SpeechToTextV1)
- description and source-code
```javascript
function SpeechToTextV1(options) {
  BaseService.call(this, options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.TextToSpeechV1"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.</span>TextToSpeechV1 (options)](#apidoc.element.watson-developer-cloud.TextToSpeechV1)
- description and source-code
```javascript
function TextToSpeechV1(options) {
  BaseService.call(this, options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.ToneAnalyzerV3"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.</span>ToneAnalyzerV3 (options)](#apidoc.element.watson-developer-cloud.ToneAnalyzerV3)
- description and source-code
```javascript
function ToneAnalyzerV3(options) {
  BaseService.call(this, options);
  // Check if 'version_date' was provided
  if (typeof this._options.version_date === 'undefined') {
    throw new Error('Argument error: version_date was not specified, use 2016-05-19');
  }
  // todo: confirm that the service wants version, not version_date
  this._options.qs.version = this._options.version_date;
}
```
- example usage
```shell
...
The following methods will also work, but cause the entire library to be loaded:

'''js
// Alternate methods of using the library.
// Not recommended, especially for client-side JS.
var watson = require('watson-developer-cloud');

var toneAnalyzer = new watson.ToneAnalyzerV3({/*...*/});

var tone_analyzer = watson.tone_analyzer({version: 'v3', /*...*/});
'''

## Installation

'''sh
...
```

#### <a name="apidoc.element.watson-developer-cloud.TradeoffAnalyticsV1"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.</span>TradeoffAnalyticsV1 (options)](#apidoc.element.watson-developer-cloud.TradeoffAnalyticsV1)
- description and source-code
```javascript
function TradeoffAnalyticsV1(options) {
  BaseService.call(this, options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.VisualRecognitionV3"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.</span>VisualRecognitionV3 (options)](#apidoc.element.watson-developer-cloud.VisualRecognitionV3)
- description and source-code
```javascript
function VisualRecognitionV3(options) {
  BaseService.call(this, options);
  // Check if 'version_date' was provided
  if (typeof this._options.version_date === 'undefined') {
    throw new Error('Argument error: version_date was not specified, use 2016-05-20');
  }
  this._options.qs.version = this._options.version_date; // todo: confirm service expects version not version_date
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.recognize_stream"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.</span>recognize_stream (options)](#apidoc.element.watson-developer-cloud.recognize_stream)
- description and source-code
```javascript
function RecognizeStream(options) {
  Duplex.call(this, options);
  this.options = options;
  this.listening = false;
  this.initialized = false;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.watson-developer-cloud.AlchemyDataNewsV1"></a>[module watson-developer-cloud.AlchemyDataNewsV1](#apidoc.module.watson-developer-cloud.AlchemyDataNewsV1)

#### <a name="apidoc.element.watson-developer-cloud.AlchemyDataNewsV1.AlchemyDataNewsV1"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.</span>AlchemyDataNewsV1 (options)](#apidoc.element.watson-developer-cloud.AlchemyDataNewsV1.AlchemyDataNewsV1)
- description and source-code
```javascript
function AlchemyDataNewsV1(options) {
  BaseServiceAlchemy.call(this, options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.AlchemyDataNewsV1.super_"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.AlchemyDataNewsV1.</span>super_ (options)](#apidoc.element.watson-developer-cloud.AlchemyDataNewsV1.super_)
- description and source-code
```javascript
function BaseServiceAlchemy(options) {
  BaseService.call(this, options);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.watson-developer-cloud.AlchemyDataNewsV1.prototype"></a>[module watson-developer-cloud.AlchemyDataNewsV1.prototype](#apidoc.module.watson-developer-cloud.AlchemyDataNewsV1.prototype)

#### <a name="apidoc.element.watson-developer-cloud.AlchemyDataNewsV1.prototype.getNews"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.AlchemyDataNewsV1.prototype.</span>getNews (params, callback)](#apidoc.element.watson-developer-cloud.AlchemyDataNewsV1.prototype.getNews)
- description and source-code
```javascript
getNews = function (params, callback) {
  params = params || {};

  const parameters = {
    options: {
      url: '/data/GetNews',
      method: 'GET',
      json: true,
      qs: extend({}, params, { outputMode: 'json' }) // change default output to json
    },
    requiredParams: ['end', 'start'],
    defaultOptions: this._options
  };
  return requestFactory(parameters, errorFormatter(callback));
}
```
- example usage
```shell
...
});

var params = {
  start: 'now-1d',
  end: 'now'
};

alchemy_data_news.getNews(params, function (err, news) {
  if (err)
    console.log('error:', err);
  else
    console.log(JSON.stringify(news, null, 2));
});
'''
...
```



# <a name="apidoc.module.watson-developer-cloud.AlchemyDataNewsV1.super_"></a>[module watson-developer-cloud.AlchemyDataNewsV1.super_](#apidoc.module.watson-developer-cloud.AlchemyDataNewsV1.super_)

#### <a name="apidoc.element.watson-developer-cloud.AlchemyDataNewsV1.super_.super_"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.AlchemyDataNewsV1.</span>super_ (user_options)](#apidoc.element.watson-developer-cloud.AlchemyDataNewsV1.super_.super_)
- description and source-code
```javascript
function BaseService(user_options) {
  if (!(this instanceof BaseService)) {
    // it might be better to just create a new instance and return that.. but that can't be done here, it has to be done in each
 individual service. So this is still a good failsafe even in that case.
    throw new Error('"new" keyword required to create Watson service instances');
  }
  let options = extend({}, user_options);

  options = this.initCredentials(options);

  if (options.url) {
    options.url = helper.stripTrailingSlash(options.url);
  }

  this._options = extend({ qs: {}, url: this.constructor.URL }, this.serviceDefaults, options);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.watson-developer-cloud.AlchemyDataNewsV1.super_.prototype"></a>[module watson-developer-cloud.AlchemyDataNewsV1.super_.prototype](#apidoc.module.watson-developer-cloud.AlchemyDataNewsV1.super_.prototype)

#### <a name="apidoc.element.watson-developer-cloud.AlchemyDataNewsV1.super_.prototype.getCredentials"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.AlchemyDataNewsV1.super_.prototype.</span>getCredentials ()](#apidoc.element.watson-developer-cloud.AlchemyDataNewsV1.super_.prototype.getCredentials)
- description and source-code
```javascript
getCredentials = function () {
  return {
    apikey: this._options.apikey,
    url: this._options.url
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.AlchemyDataNewsV1.super_.prototype.getCredentialsFromEnvironment"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.AlchemyDataNewsV1.super_.prototype.</span>getCredentialsFromEnvironment (name)](#apidoc.element.watson-developer-cloud.AlchemyDataNewsV1.super_.prototype.getCredentialsFromEnvironment)
- description and source-code
```javascript
getCredentialsFromEnvironment = function (name) {
  return {
    apikey: process.env[name.toUpperCase() + '_API_KEY'],
    url: process.env[name + '_URL']
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.AlchemyDataNewsV1.super_.prototype.initCredentials"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.AlchemyDataNewsV1.super_.prototype.</span>initCredentials (options)](#apidoc.element.watson-developer-cloud.AlchemyDataNewsV1.super_.prototype.initCredentials)
- description and source-code
```javascript
initCredentials = function (options) {
  options.apikey = options.apikey || options.api_key;
  options = extend(
    {},
    this.getCredentialsFromBluemix('alchemy_api'), // this is the same for all Alchemy* services
    this.getCredentialsFromEnvironment(this.name),
    options
  );
  if (!options.use_unauthenticated) {
    if (!options.apikey) {
      throw new Error('Argument error: api_key was not specified');
    }
    // Per documentation, Alchemy* services use 'apikey', but Visual Recognition uses ('api_key')
    // (Either will work in most cases, but there are a few exceptions.)
    options.qs = extend({ apikey: options.apikey }, options.qs);
  }
  return options;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.watson-developer-cloud.AlchemyLanguageV1"></a>[module watson-developer-cloud.AlchemyLanguageV1](#apidoc.module.watson-developer-cloud.AlchemyLanguageV1)

#### <a name="apidoc.element.watson-developer-cloud.AlchemyLanguageV1.AlchemyLanguageV1"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.</span>AlchemyLanguageV1 (options)](#apidoc.element.watson-developer-cloud.AlchemyLanguageV1.AlchemyLanguageV1)
- description and source-code
```javascript
function AlchemyLanguageV1(options) {
  BaseServiceAlchemy.call(this, options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.AlchemyLanguageV1.super_"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.AlchemyLanguageV1.</span>super_ (options)](#apidoc.element.watson-developer-cloud.AlchemyLanguageV1.super_)
- description and source-code
```javascript
function BaseServiceAlchemy(options) {
  BaseService.call(this, options);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.watson-developer-cloud.AlchemyLanguageV1.prototype"></a>[module watson-developer-cloud.AlchemyLanguageV1.prototype](#apidoc.module.watson-developer-cloud.AlchemyLanguageV1.prototype)

#### <a name="apidoc.element.watson-developer-cloud.AlchemyLanguageV1.prototype.authors"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.AlchemyLanguageV1.prototype.</span>authors (_params, callback)](#apidoc.element.watson-developer-cloud.AlchemyLanguageV1.prototype.authors)
- description and source-code
```javascript
authors = function (_params, callback) {
  const params = _params || {};
  const accepted_formats = Object.keys(endpoints[method]);
  const format = helper.getFormat(params, accepted_formats);

  if (format === null) {
    callback(new Error('Missing required parameters: ' + accepted_formats.join(', ') + ' needs to be specified'));
    return;
  }

  const parameters = {
    options: {
      url: endpoints[method][format],
      method: 'POST',
      json: true,
      qs: pick(params, ['model']),
      form: extend({}, params, { outputMode: 'json' }) // change default output to json
    },
    defaultOptions: this._options // eslint-disable-line no-invalid-this
  };
  return requestFactory(parameters, errorFormatter(callback));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.AlchemyLanguageV1.prototype.category"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.AlchemyLanguageV1.prototype.</span>category (_params, callback)](#apidoc.element.watson-developer-cloud.AlchemyLanguageV1.prototype.category)
- description and source-code
```javascript
category = function (_params, callback) {
  const params = _params || {};
  const accepted_formats = Object.keys(endpoints[method]);
  const format = helper.getFormat(params, accepted_formats);

  if (format === null) {
    callback(new Error('Missing required parameters: ' + accepted_formats.join(', ') + ' needs to be specified'));
    return;
  }

  const parameters = {
    options: {
      url: endpoints[method][format],
      method: 'POST',
      json: true,
      qs: pick(params, ['model']),
      form: extend({}, params, { outputMode: 'json' }) // change default output to json
    },
    defaultOptions: this._options // eslint-disable-line no-invalid-this
  };
  return requestFactory(parameters, errorFormatter(callback));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.AlchemyLanguageV1.prototype.combined"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.AlchemyLanguageV1.prototype.</span>combined (_params, callback)](#apidoc.element.watson-developer-cloud.AlchemyLanguageV1.prototype.combined)
- description and source-code
```javascript
combined = function (_params, callback) {
  const params = _params || {};
  const accepted_formats = Object.keys(endpoints[method]);
  const format = helper.getFormat(params, accepted_formats);

  if (format === null) {
    callback(new Error('Missing required parameters: ' + accepted_formats.join(', ') + ' needs to be specified'));
    return;
  }

  const parameters = {
    options: {
      url: endpoints[method][format],
      method: 'POST',
      json: true,
      qs: pick(params, ['model']),
      form: extend({}, params, { outputMode: 'json' }) // change default output to json
    },
    defaultOptions: this._options // eslint-disable-line no-invalid-this
  };
  return requestFactory(parameters, errorFormatter(callback));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.AlchemyLanguageV1.prototype.concepts"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.AlchemyLanguageV1.prototype.</span>concepts (_params, callback)](#apidoc.element.watson-developer-cloud.AlchemyLanguageV1.prototype.concepts)
- description and source-code
```javascript
concepts = function (_params, callback) {
  const params = _params || {};
  const accepted_formats = Object.keys(endpoints[method]);
  const format = helper.getFormat(params, accepted_formats);

  if (format === null) {
    callback(new Error('Missing required parameters: ' + accepted_formats.join(', ') + ' needs to be specified'));
    return;
  }

  const parameters = {
    options: {
      url: endpoints[method][format],
      method: 'POST',
      json: true,
      qs: pick(params, ['model']),
      form: extend({}, params, { outputMode: 'json' }) // change default output to json
    },
    defaultOptions: this._options // eslint-disable-line no-invalid-this
  };
  return requestFactory(parameters, errorFormatter(callback));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.AlchemyLanguageV1.prototype.dates"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.AlchemyLanguageV1.prototype.</span>dates (_params, callback)](#apidoc.element.watson-developer-cloud.AlchemyLanguageV1.prototype.dates)
- description and source-code
```javascript
dates = function (_params, callback) {
  const params = _params || {};
  const accepted_formats = Object.keys(endpoints[method]);
  const format = helper.getFormat(params, accepted_formats);

  if (format === null) {
    callback(new Error('Missing required parameters: ' + accepted_formats.join(', ') + ' needs to be specified'));
    return;
  }

  const parameters = {
    options: {
      url: endpoints[method][format],
      method: 'POST',
      json: true,
      qs: pick(params, ['model']),
      form: extend({}, params, { outputMode: 'json' }) // change default output to json
    },
    defaultOptions: this._options // eslint-disable-line no-invalid-this
  };
  return requestFactory(parameters, errorFormatter(callback));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.AlchemyLanguageV1.prototype.emotion"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.AlchemyLanguageV1.prototype.</span>emotion (params, callback)](#apidoc.element.watson-developer-cloud.AlchemyLanguageV1.prototype.emotion)
- description and source-code
```javascript
emotion = function (params, callback) {
  const _params = extend({}, params);
  const service = params.target || params.targets ? 'emotion_targeted' : 'emotion';
  if (Array.isArray(_params.targets)) {
    _params.targets = _params.targets.join('|');
  }

  return createRequest(service).call(this, _params, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.AlchemyLanguageV1.prototype.entities"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.AlchemyLanguageV1.prototype.</span>entities (_params, callback)](#apidoc.element.watson-developer-cloud.AlchemyLanguageV1.prototype.entities)
- description and source-code
```javascript
entities = function (_params, callback) {
  const params = _params || {};
  const accepted_formats = Object.keys(endpoints[method]);
  const format = helper.getFormat(params, accepted_formats);

  if (format === null) {
    callback(new Error('Missing required parameters: ' + accepted_formats.join(', ') + ' needs to be specified'));
    return;
  }

  const parameters = {
    options: {
      url: endpoints[method][format],
      method: 'POST',
      json: true,
      qs: pick(params, ['model']),
      form: extend({}, params, { outputMode: 'json' }) // change default output to json
    },
    defaultOptions: this._options // eslint-disable-line no-invalid-this
  };
  return requestFactory(parameters, errorFormatter(callback));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.AlchemyLanguageV1.prototype.feeds"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.AlchemyLanguageV1.prototype.</span>feeds (_params, callback)](#apidoc.element.watson-developer-cloud.AlchemyLanguageV1.prototype.feeds)
- description and source-code
```javascript
feeds = function (_params, callback) {
  const params = _params || {};
  const accepted_formats = Object.keys(endpoints[method]);
  const format = helper.getFormat(params, accepted_formats);

  if (format === null) {
    callback(new Error('Missing required parameters: ' + accepted_formats.join(', ') + ' needs to be specified'));
    return;
  }

  const parameters = {
    options: {
      url: endpoints[method][format],
      method: 'POST',
      json: true,
      qs: pick(params, ['model']),
      form: extend({}, params, { outputMode: 'json' }) // change default output to json
    },
    defaultOptions: this._options // eslint-disable-line no-invalid-this
  };
  return requestFactory(parameters, errorFormatter(callback));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.AlchemyLanguageV1.prototype.keywords"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.AlchemyLanguageV1.prototype.</span>keywords (_params, callback)](#apidoc.element.watson-developer-cloud.AlchemyLanguageV1.prototype.keywords)
- description and source-code
```javascript
keywords = function (_params, callback) {
  const params = _params || {};
  const accepted_formats = Object.keys(endpoints[method]);
  const format = helper.getFormat(params, accepted_formats);

  if (format === null) {
    callback(new Error('Missing required parameters: ' + accepted_formats.join(', ') + ' needs to be specified'));
    return;
  }

  const parameters = {
    options: {
      url: endpoints[method][format],
      method: 'POST',
      json: true,
      qs: pick(params, ['model']),
      form: extend({}, params, { outputMode: 'json' }) // change default output to json
    },
    defaultOptions: this._options // eslint-disable-line no-invalid-this
  };
  return requestFactory(parameters, errorFormatter(callback));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.AlchemyLanguageV1.prototype.language"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.AlchemyLanguageV1.prototype.</span>language (_params, callback)](#apidoc.element.watson-developer-cloud.AlchemyLanguageV1.prototype.language)
- description and source-code
```javascript
language = function (_params, callback) {
  const params = _params || {};
  const accepted_formats = Object.keys(endpoints[method]);
  const format = helper.getFormat(params, accepted_formats);

  if (format === null) {
    callback(new Error('Missing required parameters: ' + accepted_formats.join(', ') + ' needs to be specified'));
    return;
  }

  const parameters = {
    options: {
      url: endpoints[method][format],
      method: 'POST',
      json: true,
      qs: pick(params, ['model']),
      form: extend({}, params, { outputMode: 'json' }) // change default output to json
    },
    defaultOptions: this._options // eslint-disable-line no-invalid-this
  };
  return requestFactory(parameters, errorFormatter(callback));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.AlchemyLanguageV1.prototype.microformats"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.AlchemyLanguageV1.prototype.</span>microformats (_params, callback)](#apidoc.element.watson-developer-cloud.AlchemyLanguageV1.prototype.microformats)
- description and source-code
```javascript
microformats = function (_params, callback) {
  const params = _params || {};
  const accepted_formats = Object.keys(endpoints[method]);
  const format = helper.getFormat(params, accepted_formats);

  if (format === null) {
    callback(new Error('Missing required parameters: ' + accepted_formats.join(', ') + ' needs to be specified'));
    return;
  }

  const parameters = {
    options: {
      url: endpoints[method][format],
      method: 'POST',
      json: true,
      qs: pick(params, ['model']),
      form: extend({}, params, { outputMode: 'json' }) // change default output to json
    },
    defaultOptions: this._options // eslint-disable-line no-invalid-this
  };
  return requestFactory(parameters, errorFormatter(callback));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.AlchemyLanguageV1.prototype.publicationDate"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.AlchemyLanguageV1.prototype.</span>publicationDate (_params, callback)](#apidoc.element.watson-developer-cloud.AlchemyLanguageV1.prototype.publicationDate)
- description and source-code
```javascript
publicationDate = function (_params, callback) {
  const params = _params || {};
  const accepted_formats = Object.keys(endpoints[method]);
  const format = helper.getFormat(params, accepted_formats);

  if (format === null) {
    callback(new Error('Missing required parameters: ' + accepted_formats.join(', ') + ' needs to be specified'));
    return;
  }

  const parameters = {
    options: {
      url: endpoints[method][format],
      method: 'POST',
      json: true,
      qs: pick(params, ['model']),
      form: extend({}, params, { outputMode: 'json' }) // change default output to json
    },
    defaultOptions: this._options // eslint-disable-line no-invalid-this
  };
  return requestFactory(parameters, errorFormatter(callback));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.AlchemyLanguageV1.prototype.relations"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.AlchemyLanguageV1.prototype.</span>relations (_params, callback)](#apidoc.element.watson-developer-cloud.AlchemyLanguageV1.prototype.relations)
- description and source-code
```javascript
relations = function (_params, callback) {
  const params = _params || {};
  const accepted_formats = Object.keys(endpoints[method]);
  const format = helper.getFormat(params, accepted_formats);

  if (format === null) {
    callback(new Error('Missing required parameters: ' + accepted_formats.join(', ') + ' needs to be specified'));
    return;
  }

  const parameters = {
    options: {
      url: endpoints[method][format],
      method: 'POST',
      json: true,
      qs: pick(params, ['model']),
      form: extend({}, params, { outputMode: 'json' }) // change default output to json
    },
    defaultOptions: this._options // eslint-disable-line no-invalid-this
  };
  return requestFactory(parameters, errorFormatter(callback));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.AlchemyLanguageV1.prototype.sentiment"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.AlchemyLanguageV1.prototype.</span>sentiment (params, callback)](#apidoc.element.watson-developer-cloud.AlchemyLanguageV1.prototype.sentiment)
- description and source-code
```javascript
sentiment = function (params, callback) {
  const _params = extend({}, params);
  const service = params.target || params.targets ? 'sentiment_targeted' : 'sentiment';
  if (Array.isArray(_params.targets)) {
    _params.targets = _params.targets.join('|');
  }

  return createRequest(service).call(this, _params, callback);
}
```
- example usage
```shell
...
  api_key: 'API_KEY'
});

var params = {
  text: 'IBM Watson won the Jeopardy television show hosted by Alex Trebek'
};

alchemy_language.sentiment(params, function (err, response) {
  if (err)
    console.log('error:', err);
  else
    console.log(JSON.stringify(response, null, 2));
});
'''
...
```

#### <a name="apidoc.element.watson-developer-cloud.AlchemyLanguageV1.prototype.taxonomy"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.AlchemyLanguageV1.prototype.</span>taxonomy (_params, callback)](#apidoc.element.watson-developer-cloud.AlchemyLanguageV1.prototype.taxonomy)
- description and source-code
```javascript
taxonomy = function (_params, callback) {
  const params = _params || {};
  const accepted_formats = Object.keys(endpoints[method]);
  const format = helper.getFormat(params, accepted_formats);

  if (format === null) {
    callback(new Error('Missing required parameters: ' + accepted_formats.join(', ') + ' needs to be specified'));
    return;
  }

  const parameters = {
    options: {
      url: endpoints[method][format],
      method: 'POST',
      json: true,
      qs: pick(params, ['model']),
      form: extend({}, params, { outputMode: 'json' }) // change default output to json
    },
    defaultOptions: this._options // eslint-disable-line no-invalid-this
  };
  return requestFactory(parameters, errorFormatter(callback));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.AlchemyLanguageV1.prototype.text"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.AlchemyLanguageV1.prototype.</span>text (params, callback)](#apidoc.element.watson-developer-cloud.AlchemyLanguageV1.prototype.text)
- description and source-code
```javascript
text = function (params, callback) {
  const service = params && params.raw ? 'text_raw' : 'text';
  return createRequest(service).call(this, params, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.AlchemyLanguageV1.prototype.title"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.AlchemyLanguageV1.prototype.</span>title (_params, callback)](#apidoc.element.watson-developer-cloud.AlchemyLanguageV1.prototype.title)
- description and source-code
```javascript
title = function (_params, callback) {
  const params = _params || {};
  const accepted_formats = Object.keys(endpoints[method]);
  const format = helper.getFormat(params, accepted_formats);

  if (format === null) {
    callback(new Error('Missing required parameters: ' + accepted_formats.join(', ') + ' needs to be specified'));
    return;
  }

  const parameters = {
    options: {
      url: endpoints[method][format],
      method: 'POST',
      json: true,
      qs: pick(params, ['model']),
      form: extend({}, params, { outputMode: 'json' }) // change default output to json
    },
    defaultOptions: this._options // eslint-disable-line no-invalid-this
  };
  return requestFactory(parameters, errorFormatter(callback));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.AlchemyLanguageV1.prototype.typedRelations"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.AlchemyLanguageV1.prototype.</span>typedRelations (_params, callback)](#apidoc.element.watson-developer-cloud.AlchemyLanguageV1.prototype.typedRelations)
- description and source-code
```javascript
typedRelations = function (_params, callback) {
  const params = _params || {};
  const accepted_formats = Object.keys(endpoints[method]);
  const format = helper.getFormat(params, accepted_formats);

  if (format === null) {
    callback(new Error('Missing required parameters: ' + accepted_formats.join(', ') + ' needs to be specified'));
    return;
  }

  const parameters = {
    options: {
      url: endpoints[method][format],
      method: 'POST',
      json: true,
      qs: pick(params, ['model']),
      form: extend({}, params, { outputMode: 'json' }) // change default output to json
    },
    defaultOptions: this._options // eslint-disable-line no-invalid-this
  };
  return requestFactory(parameters, errorFormatter(callback));
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.watson-developer-cloud.AlchemyVisionV1"></a>[module watson-developer-cloud.AlchemyVisionV1](#apidoc.module.watson-developer-cloud.AlchemyVisionV1)

#### <a name="apidoc.element.watson-developer-cloud.AlchemyVisionV1.AlchemyVisionV1"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.</span>AlchemyVisionV1 (options)](#apidoc.element.watson-developer-cloud.AlchemyVisionV1.AlchemyVisionV1)
- description and source-code
```javascript
function AlchemyVisionV1(options) {
  BaseServiceAlchemy.call(this, options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.AlchemyVisionV1.super_"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.AlchemyVisionV1.</span>super_ (options)](#apidoc.element.watson-developer-cloud.AlchemyVisionV1.super_)
- description and source-code
```javascript
function BaseServiceAlchemy(options) {
  BaseService.call(this, options);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.watson-developer-cloud.AlchemyVisionV1.prototype"></a>[module watson-developer-cloud.AlchemyVisionV1.prototype](#apidoc.module.watson-developer-cloud.AlchemyVisionV1.prototype)

#### <a name="apidoc.element.watson-developer-cloud.AlchemyVisionV1.prototype.getImageKeywords"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.AlchemyVisionV1.prototype.</span>getImageKeywords (_params, callback)](#apidoc.element.watson-developer-cloud.AlchemyVisionV1.prototype.getImageKeywords)
- description and source-code
```javascript
getImageKeywords = function (_params, callback) {
  const params = _params || {};
  const accepted_formats = Object.keys(endpoints[method]);
  const format = helper.getFormat(params, accepted_formats);

  if (format === null) {
    callback(new Error('Missing required parameters: ' + accepted_formats.join(', ') + ' needs to be specified'));
    return;
  }
  // always return json
  params.outputMode = 'json';

  const parameters = {
    options: {
      url: endpoints[method][format],
      method: 'POST'
    },
    defaultOptions: this._options // eslint-disable-line no-invalid-this
  };

  if (!params.image || !isStream(params.image)) {
    // url or base64 images are considered 'not-raw'
    if (params.image) {
      params.imagePostMode = 'not-raw';
    }
    // send the parameters as form url-encoded
    parameters.options.form = params;
    return requestFactory(parameters, errorFormatter(callback));
  } else {
    params.imagePostMode = 'raw';
    // send the parameters as query parameters
    parameters.options.qs = omit(params, ['image']);
    // add the content-length to the headers
    parameters.options.headers = {
      'Content-Length': fs.statSync(params.image.path).size
    };
    return params.image.pipe(requestFactory(parameters, errorFormatter(callback)));
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.AlchemyVisionV1.prototype.getImageLinks"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.AlchemyVisionV1.prototype.</span>getImageLinks (_params, callback)](#apidoc.element.watson-developer-cloud.AlchemyVisionV1.prototype.getImageLinks)
- description and source-code
```javascript
getImageLinks = function (_params, callback) {
  const params = _params || {};
  const accepted_formats = Object.keys(endpoints[method]);
  const format = helper.getFormat(params, accepted_formats);

  if (format === null) {
    callback(new Error('Missing required parameters: ' + accepted_formats.join(', ') + ' needs to be specified'));
    return;
  }
  // always return json
  params.outputMode = 'json';

  const parameters = {
    options: {
      url: endpoints[method][format],
      method: 'POST'
    },
    defaultOptions: this._options // eslint-disable-line no-invalid-this
  };

  if (!params.image || !isStream(params.image)) {
    // url or base64 images are considered 'not-raw'
    if (params.image) {
      params.imagePostMode = 'not-raw';
    }
    // send the parameters as form url-encoded
    parameters.options.form = params;
    return requestFactory(parameters, errorFormatter(callback));
  } else {
    params.imagePostMode = 'raw';
    // send the parameters as query parameters
    parameters.options.qs = omit(params, ['image']);
    // add the content-length to the headers
    parameters.options.headers = {
      'Content-Length': fs.statSync(params.image.path).size
    };
    return params.image.pipe(requestFactory(parameters, errorFormatter(callback)));
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.AlchemyVisionV1.prototype.getImageSceneText"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.AlchemyVisionV1.prototype.</span>getImageSceneText (_params, callback)](#apidoc.element.watson-developer-cloud.AlchemyVisionV1.prototype.getImageSceneText)
- description and source-code
```javascript
getImageSceneText = function (_params, callback) {
  const params = _params || {};
  const accepted_formats = Object.keys(endpoints[method]);
  const format = helper.getFormat(params, accepted_formats);

  if (format === null) {
    callback(new Error('Missing required parameters: ' + accepted_formats.join(', ') + ' needs to be specified'));
    return;
  }
  // always return json
  params.outputMode = 'json';

  const parameters = {
    options: {
      url: endpoints[method][format],
      method: 'POST'
    },
    defaultOptions: this._options // eslint-disable-line no-invalid-this
  };

  if (!params.image || !isStream(params.image)) {
    // url or base64 images are considered 'not-raw'
    if (params.image) {
      params.imagePostMode = 'not-raw';
    }
    // send the parameters as form url-encoded
    parameters.options.form = params;
    return requestFactory(parameters, errorFormatter(callback));
  } else {
    params.imagePostMode = 'raw';
    // send the parameters as query parameters
    parameters.options.qs = omit(params, ['image']);
    // add the content-length to the headers
    parameters.options.headers = {
      'Content-Length': fs.statSync(params.image.path).size
    };
    return params.image.pipe(requestFactory(parameters, errorFormatter(callback)));
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.AlchemyVisionV1.prototype.recognizeFaces"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.AlchemyVisionV1.prototype.</span>recognizeFaces (_params, callback)](#apidoc.element.watson-developer-cloud.AlchemyVisionV1.prototype.recognizeFaces)
- description and source-code
```javascript
recognizeFaces = function (_params, callback) {
  const params = _params || {};
  const accepted_formats = Object.keys(endpoints[method]);
  const format = helper.getFormat(params, accepted_formats);

  if (format === null) {
    callback(new Error('Missing required parameters: ' + accepted_formats.join(', ') + ' needs to be specified'));
    return;
  }
  // always return json
  params.outputMode = 'json';

  const parameters = {
    options: {
      url: endpoints[method][format],
      method: 'POST'
    },
    defaultOptions: this._options // eslint-disable-line no-invalid-this
  };

  if (!params.image || !isStream(params.image)) {
    // url or base64 images are considered 'not-raw'
    if (params.image) {
      params.imagePostMode = 'not-raw';
    }
    // send the parameters as form url-encoded
    parameters.options.form = params;
    return requestFactory(parameters, errorFormatter(callback));
  } else {
    params.imagePostMode = 'raw';
    // send the parameters as query parameters
    parameters.options.qs = omit(params, ['image']);
    // add the content-length to the headers
    parameters.options.headers = {
      'Content-Length': fs.statSync(params.image.path).size
    };
    return params.image.pipe(requestFactory(parameters, errorFormatter(callback)));
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.watson-developer-cloud.AuthorizationV1"></a>[module watson-developer-cloud.AuthorizationV1](#apidoc.module.watson-developer-cloud.AuthorizationV1)

#### <a name="apidoc.element.watson-developer-cloud.AuthorizationV1.AuthorizationV1"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.</span>AuthorizationV1 (options)](#apidoc.element.watson-developer-cloud.AuthorizationV1.AuthorizationV1)
- description and source-code
```javascript
function AuthorizationV1(options) {
  BaseService.call(this, options);
  this.target_url = options.url;
  // replace the url to always point to /authorization/api
  const hostname = url.parse(this._options.url);
  hostname.pathname = '/authorization/api';
  this._options.url = url.format(hostname);
}
```
- example usage
```shell
...
Tokens are valid for 1 hour and may be sent using the 'X-Watson-Authorization-Token' header or the 'watson-token' query param.

Note that the token is supplied URL-encoded, and will not be accepted if it is double-encoded in a querystring.

'''javascript
var watson = require('watson-developer-cloud');

var authorization = new watson.AuthorizationV1({
username: '<Text to Speech username>',
password: '<Text to Speech password>',
url: watson.TextToSpeechV1.URL
});

authorization.getToken(function (err, token) {
if (!token) {
...
```

#### <a name="apidoc.element.watson-developer-cloud.AuthorizationV1.super_"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.AuthorizationV1.</span>super_ (user_options)](#apidoc.element.watson-developer-cloud.AuthorizationV1.super_)
- description and source-code
```javascript
function BaseService(user_options) {
  if (!(this instanceof BaseService)) {
    // it might be better to just create a new instance and return that.. but that can't be done here, it has to be done in each
 individual service. So this is still a good failsafe even in that case.
    throw new Error('"new" keyword required to create Watson service instances');
  }
  let options = extend({}, user_options);

  options = this.initCredentials(options);

  if (options.url) {
    options.url = helper.stripTrailingSlash(options.url);
  }

  this._options = extend({ qs: {}, url: this.constructor.URL }, this.serviceDefaults, options);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.watson-developer-cloud.AuthorizationV1.prototype"></a>[module watson-developer-cloud.AuthorizationV1.prototype](#apidoc.module.watson-developer-cloud.AuthorizationV1.prototype)

#### <a name="apidoc.element.watson-developer-cloud.AuthorizationV1.prototype.getToken"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.AuthorizationV1.prototype.</span>getToken (params, callback)](#apidoc.element.watson-developer-cloud.AuthorizationV1.prototype.getToken)
- description and source-code
```javascript
getToken = function (params, callback) {
  if (typeof params === 'function') {
    callback = params;
    params = { url: this.target_url };
  }
  if (!params.url) {
    callback(new Error('Missing required parameters: url'));
    return;
  }

  const parameters = {
    options: {
      method: 'GET',
      url: '/v1/token?url=' + params.url
    },
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
...

var authorization = new watson.AuthorizationV1({
  username: '<Text to Speech username>',
  password: '<Text to Speech password>',
  url: watson.TextToSpeechV1.URL
});

authorization.getToken(function (err, token) {
  if (!token) {
    console.log('error:', err);
  } else {
    // Use your token here
  }
});
'''
...
```



# <a name="apidoc.module.watson-developer-cloud.AuthorizationV1.super_"></a>[module watson-developer-cloud.AuthorizationV1.super_](#apidoc.module.watson-developer-cloud.AuthorizationV1.super_)

#### <a name="apidoc.element.watson-developer-cloud.AuthorizationV1.super_.super_"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.AuthorizationV1.</span>super_ (user_options)](#apidoc.element.watson-developer-cloud.AuthorizationV1.super_.super_)
- description and source-code
```javascript
function BaseService(user_options) {
  if (!(this instanceof BaseService)) {
    // it might be better to just create a new instance and return that.. but that can't be done here, it has to be done in each
 individual service. So this is still a good failsafe even in that case.
    throw new Error('"new" keyword required to create Watson service instances');
  }
  let options = extend({}, user_options);

  options = this.initCredentials(options);

  if (options.url) {
    options.url = helper.stripTrailingSlash(options.url);
  }

  this._options = extend({ qs: {}, url: this.constructor.URL }, this.serviceDefaults, options);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.watson-developer-cloud.AuthorizationV1.super_.prototype"></a>[module watson-developer-cloud.AuthorizationV1.super_.prototype](#apidoc.module.watson-developer-cloud.AuthorizationV1.super_.prototype)

#### <a name="apidoc.element.watson-developer-cloud.AuthorizationV1.super_.prototype.getCredentials"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.AuthorizationV1.super_.prototype.</span>getCredentials ()](#apidoc.element.watson-developer-cloud.AuthorizationV1.super_.prototype.getCredentials)
- description and source-code
```javascript
getCredentials = function () {
  return {
    username: this._options.username,
    password: this._options.password,
    url: this._options.url
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.AuthorizationV1.super_.prototype.getCredentialsFromBluemix"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.AuthorizationV1.super_.prototype.</span>getCredentialsFromBluemix (vcap_services_name)](#apidoc.element.watson-developer-cloud.AuthorizationV1.super_.prototype.getCredentialsFromBluemix)
- description and source-code
```javascript
getCredentialsFromBluemix = function (vcap_services_name) {
  return vcapServices.getCredentials(vcap_services_name);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.AuthorizationV1.super_.prototype.getCredentialsFromEnvironment"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.AuthorizationV1.super_.prototype.</span>getCredentialsFromEnvironment (name)](#apidoc.element.watson-developer-cloud.AuthorizationV1.super_.prototype.getCredentialsFromEnvironment)
- description and source-code
```javascript
getCredentialsFromEnvironment = function (name) {
  name = name.toUpperCase();
  return {
    username: process.env[name + '_USERNAME'],
    password: process.env[name + '_PASSWORD'],
    url: process.env[name + '_URL']
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.AuthorizationV1.super_.prototype.initCredentials"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.AuthorizationV1.super_.prototype.</span>initCredentials (options)](#apidoc.element.watson-developer-cloud.AuthorizationV1.super_.prototype.initCredentials)
- description and source-code
```javascript
initCredentials = function (options) {
  if (options.token) {
    options.headers = options.headers || {};
    options.headers['X-Watson-Authorization-Token'] = options.token;
    return options;
  }

  options.jar = request.jar();

  // Get credentials from environment properties or Bluemix
  // but prefer credentials provided pragmatically!
  options = extend({}, this.getCredentialsFromBluemix(this.name), this.getCredentialsFromEnvironment(this.name), options);

  if (!options.use_unauthenticated) {
    if (!options.username || !options.password) {
      throw new Error('Argument error: username and password are required unless use_unauthenticated is set');
    }

    // Calculate and add Authorization header to base options
    const authHeader = {
      Authorization: 'Basic ' + bufferFrom(options.username + ':' + options.password).toString('base64')
    };
    options.headers = extend(authHeader, options.headers);
  }

  return options;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.watson-developer-cloud.ConversationV1"></a>[module watson-developer-cloud.ConversationV1](#apidoc.module.watson-developer-cloud.ConversationV1)

#### <a name="apidoc.element.watson-developer-cloud.ConversationV1.ConversationV1"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.</span>ConversationV1 (options)](#apidoc.element.watson-developer-cloud.ConversationV1.ConversationV1)
- description and source-code
```javascript
function ConversationV1(options) {
  BaseService.call(this, options);

  // Check if 'version_date' was provided
  if (typeof this._options.version_date === 'undefined') {
    throw new Error('Argument error: version_date was not specified, use ConversationV1.VERSION_DATE_2017_02_03');
  }
  this._options.qs.version = options.version_date;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.ConversationV1.super_"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.ConversationV1.</span>super_ (user_options)](#apidoc.element.watson-developer-cloud.ConversationV1.super_)
- description and source-code
```javascript
function BaseService(user_options) {
  if (!(this instanceof BaseService)) {
    // it might be better to just create a new instance and return that.. but that can't be done here, it has to be done in each
 individual service. So this is still a good failsafe even in that case.
    throw new Error('"new" keyword required to create Watson service instances');
  }
  let options = extend({}, user_options);

  options = this.initCredentials(options);

  if (options.url) {
    options.url = helper.stripTrailingSlash(options.url);
  }

  this._options = extend({ qs: {}, url: this.constructor.URL }, this.serviceDefaults, options);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.watson-developer-cloud.ConversationV1.prototype"></a>[module watson-developer-cloud.ConversationV1.prototype](#apidoc.module.watson-developer-cloud.ConversationV1.prototype)

#### <a name="apidoc.element.watson-developer-cloud.ConversationV1.prototype.createCounterExample"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.ConversationV1.prototype.</span>createCounterExample (params, callback)](#apidoc.element.watson-developer-cloud.ConversationV1.prototype.createCounterExample)
- description and source-code
```javascript
createCounterExample = function (params, callback) {
  params = params || {};

  const parameters = {
    options: {
      url: '/v1/workspaces/{workspace_id}/counterexamples',
      method: 'POST',
      json: true,
      path: pick(params, ['workspace_id']),
      body: pick(params, ['text'])
    },
    requiredParams: ['workspace_id', 'text'],
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.ConversationV1.prototype.createExample"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.ConversationV1.prototype.</span>createExample (params, callback)](#apidoc.element.watson-developer-cloud.ConversationV1.prototype.createExample)
- description and source-code
```javascript
createExample = function (params, callback) {
  params = params || {};

  const parameters = {
    options: {
      url: '/v1/workspaces/{workspace_id}/intents/{intent}/examples',
      method: 'POST',
      json: true,
      path: pick(params, ['workspace_id', 'intent']),
      body: pick(params, ['text'])
    },
    requiredParams: ['workspace_id', 'intent'],
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.ConversationV1.prototype.createIntent"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.ConversationV1.prototype.</span>createIntent (params, callback)](#apidoc.element.watson-developer-cloud.ConversationV1.prototype.createIntent)
- description and source-code
```javascript
createIntent = function (params, callback) {
  params = params || {};

  const parameters = {
    options: {
      url: '/v1/workspaces/{workspace_id}/intents',
      method: 'POST',
      json: true,
      path: pick(params, ['workspace_id']),
      body: pick(params, ['intent', 'description', 'examples'])
    },
    requiredParams: ['workspace_id', 'intent'],
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.ConversationV1.prototype.createWorkspace"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.ConversationV1.prototype.</span>createWorkspace (params, callback)](#apidoc.element.watson-developer-cloud.ConversationV1.prototype.createWorkspace)
- description and source-code
```javascript
createWorkspace = function (params, callback) {
  params = params || {};

  const parameters = {
    options: {
      url: '/v1/workspaces',
      method: 'POST',
      json: true,
      body: pick(params, ['name', 'language', 'entities', 'intents', 'dialog_nodes', 'metadata', 'description', 'counterexamples
'])
    },
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.ConversationV1.prototype.deleteCounterExample"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.ConversationV1.prototype.</span>deleteCounterExample (params, callback)](#apidoc.element.watson-developer-cloud.ConversationV1.prototype.deleteCounterExample)
- description and source-code
```javascript
deleteCounterExample = function (params, callback) {
  params = params || {};

  const parameters = {
    options: {
      url: '/v1/workspaces/{workspace_id}/counterexamples/{text}',
      method: 'DELETE',
      json: true,
      path: pick(params, ['workspace_id', 'text'])
    },
    requiredParams: ['workspace_id', 'text'],
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.ConversationV1.prototype.deleteExample"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.ConversationV1.prototype.</span>deleteExample (params, callback)](#apidoc.element.watson-developer-cloud.ConversationV1.prototype.deleteExample)
- description and source-code
```javascript
deleteExample = function (params, callback) {
  params = params || {};

  const parameters = {
    options: {
      url: '/v1/workspaces/{workspace_id}/intents/{intent}/examples/{text}',
      method: 'DELETE',
      json: true,
      path: pick(params, ['workspace_id', 'intent', 'text'])
    },
    requiredParams: ['workspace_id', 'intent', 'text'],
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.ConversationV1.prototype.deleteIntent"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.ConversationV1.prototype.</span>deleteIntent (params, callback)](#apidoc.element.watson-developer-cloud.ConversationV1.prototype.deleteIntent)
- description and source-code
```javascript
deleteIntent = function (params, callback) {
  params = params || {};

  const parameters = {
    options: {
      url: '/v1/workspaces/{workspace_id}/intents/{intent}',
      method: 'DELETE',
      json: true,
      path: pick(params, ['workspace_id', 'intent'])
    },
    requiredParams: ['workspace_id', 'intent'],
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.ConversationV1.prototype.deleteWorkspace"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.ConversationV1.prototype.</span>deleteWorkspace (params, callback)](#apidoc.element.watson-developer-cloud.ConversationV1.prototype.deleteWorkspace)
- description and source-code
```javascript
deleteWorkspace = function (params, callback) {
  params = params || {};

  const parameters = {
    options: {
      url: '/v1/workspaces/{workspace_id}',
      method: 'DELETE',
      json: true,
      path: pick(params, ['workspace_id'])
    },
    requiredParams: ['workspace_id'],
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.ConversationV1.prototype.getCounterExample"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.ConversationV1.prototype.</span>getCounterExample (params, callback)](#apidoc.element.watson-developer-cloud.ConversationV1.prototype.getCounterExample)
- description and source-code
```javascript
getCounterExample = function (params, callback) {
  params = params || {};

  const parameters = {
    options: {
      url: '/v1/workspaces/{workspace_id}/counterexamples/{text}',
      method: 'GET',
      json: true,
      path: pick(params, ['workspace_id', 'text'])
    },
    requiredParams: ['workspace_id', 'text'],
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.ConversationV1.prototype.getCounterExamples"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.ConversationV1.prototype.</span>getCounterExamples (params, callback)](#apidoc.element.watson-developer-cloud.ConversationV1.prototype.getCounterExamples)
- description and source-code
```javascript
getCounterExamples = function (params, callback) {
  params = params || {};

  const parameters = {
    options: {
      url: '/v1/workspaces/{workspace_id}/counterexamples',
      method: 'GET',
      json: true,
      path: pick(params, ['workspace_id']),
      qs: pick(params, ['page_limit', 'include_count', 'sort', 'cursor'])
    },
    requiredParams: ['workspace_id'],
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.ConversationV1.prototype.getExample"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.ConversationV1.prototype.</span>getExample (params, callback)](#apidoc.element.watson-developer-cloud.ConversationV1.prototype.getExample)
- description and source-code
```javascript
getExample = function (params, callback) {
  params = params || {};

  const parameters = {
    options: {
      url: '/v1/workspaces/{workspace_id}/intents/{intent}/examples/{text}',
      method: 'GET',
      json: true,
      path: pick(params, ['workspace_id', 'intent', 'text'])
    },
    requiredParams: ['workspace_id', 'intent', 'text'],
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.ConversationV1.prototype.getExamples"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.ConversationV1.prototype.</span>getExamples (params, callback)](#apidoc.element.watson-developer-cloud.ConversationV1.prototype.getExamples)
- description and source-code
```javascript
getExamples = function (params, callback) {
  params = params || {};

  const parameters = {
    options: {
      url: '/v1/workspaces/{workspace_id}/intents/{intent}/examples',
      method: 'GET',
      json: true,
      path: pick(params, ['workspace_id', 'intent']),
      qs: pick(params, ['page_limit', 'include_count', 'sort', 'cursor'])
    },
    requiredParams: ['workspace_id', 'intent'],
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.ConversationV1.prototype.getIntent"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.ConversationV1.prototype.</span>getIntent (params, callback)](#apidoc.element.watson-developer-cloud.ConversationV1.prototype.getIntent)
- description and source-code
```javascript
getIntent = function (params, callback) {
  params = params || {};

  const parameters = {
    options: {
      url: '/v1/workspaces/{workspace_id}/intents/{intent}',
      method: 'GET',
      json: true,
      path: pick(params, ['workspace_id', 'intent']),
      qs: pick(params, ['export'])
    },
    requiredParams: ['workspace_id', 'intent'],
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.ConversationV1.prototype.getIntents"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.ConversationV1.prototype.</span>getIntents (params, callback)](#apidoc.element.watson-developer-cloud.ConversationV1.prototype.getIntents)
- description and source-code
```javascript
getIntents = function (params, callback) {
  params = params || {};

  const parameters = {
    options: {
      url: '/v1/workspaces/{workspace_id}/intents',
      method: 'GET',
      json: true,
      path: pick(params, ['workspace_id']),
      qs: pick(params, ['export', 'page_limit', 'include_count', 'sort', 'cursor'])
    },
    requiredParams: ['workspace_id'],
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.ConversationV1.prototype.getWorkspace"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.ConversationV1.prototype.</span>getWorkspace (params, callback)](#apidoc.element.watson-developer-cloud.ConversationV1.prototype.getWorkspace)
- description and source-code
```javascript
getWorkspace = function (params, callback) {
  params = params || {};

  const parameters = {
    options: {
      url: '/v1/workspaces/{workspace_id}',
      method: 'GET',
      json: true,
      qs: pick(params, ['export']),
      path: pick(params, ['workspace_id'])
    },
    requiredParams: ['workspace_id'],
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.ConversationV1.prototype.listWorkspaces"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.ConversationV1.prototype.</span>listWorkspaces (params, callback)](#apidoc.element.watson-developer-cloud.ConversationV1.prototype.listWorkspaces)
- description and source-code
```javascript
listWorkspaces = function (params, callback) {
  if (typeof params === 'function' && !callback) {
    callback = params;
    params = null;
  }
  const parameters = {
    options: {
      url: '/v1/workspaces',
      method: 'GET',
      qs: pick(params, ['page_limit', 'include_count', 'sort', 'cursor'])
    },
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.ConversationV1.prototype.message"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.ConversationV1.prototype.</span>message (params, callback)](#apidoc.element.watson-developer-cloud.ConversationV1.prototype.message)
- description and source-code
```javascript
message = function (params, callback) {
  params = params || {};

  const parameters = {
    options: {
      url: '/v1/workspaces/{workspace_id}/message',
      method: 'POST',
      json: true,
      body: pick(params, ['input', 'context', 'alternate_intents', 'output', 'entities', 'intents']),
      path: pick(params, ['workspace_id'])
    },
    requiredParams: ['workspace_id'],
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
...

var conversation = new ConversationV1({
 username: '<username>',
 password: '<password>',
 version_date: ConversationV1.VERSION_DATE_2017_02_03
});

conversation.message({
 input: { text: 'What\'s the weather?' },
 workspace_id: '<workspace id>'
}, function(err, response) {
    if (err) {
      console.error(err);
    } else {
      console.log(JSON.stringify(response, null, 2));
...
```

#### <a name="apidoc.element.watson-developer-cloud.ConversationV1.prototype.updateCounterExample"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.ConversationV1.prototype.</span>updateCounterExample (params, callback)](#apidoc.element.watson-developer-cloud.ConversationV1.prototype.updateCounterExample)
- description and source-code
```javascript
updateCounterExample = function (params, callback) {
  params = params || {};

  const parameters = {
    options: {
      url: '/v1/workspaces/{workspace_id}/counterexamples/{old_text}',
      method: 'POST',
      json: true,
      path: pick(params, ['workspace_id', 'old_text']),
      body: pick(params, ['text'])
    },
    requiredParams: ['workspace_id', 'old_text', 'text'],
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.ConversationV1.prototype.updateExample"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.ConversationV1.prototype.</span>updateExample (params, callback)](#apidoc.element.watson-developer-cloud.ConversationV1.prototype.updateExample)
- description and source-code
```javascript
updateExample = function (params, callback) {
  params = params || {};

  const parameters = {
    options: {
      url: '/v1/workspaces/{workspace_id}/intents/{intent}/examples/{old_text}',
      method: 'POST',
      json: true,
      path: pick(params, ['workspace_id', 'intent', 'old_text']),
      body: pick(params, ['text'])
    },
    requiredParams: ['workspace_id', 'intent', 'old_text', 'text'],
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.ConversationV1.prototype.updateIntent"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.ConversationV1.prototype.</span>updateIntent (params, callback)](#apidoc.element.watson-developer-cloud.ConversationV1.prototype.updateIntent)
- description and source-code
```javascript
updateIntent = function (params, callback) {
  params = params || {};

  const parameters = {
    options: {
      url: '/v1/workspaces/{workspace_id}/intents/{old_intent}',
      method: 'POST',
      json: true,
      path: pick(params, ['workspace_id', 'old_intent']),
      body: pick(params, ['intent', 'description', 'examples'])
    },
    requiredParams: ['workspace_id', 'old_intent', 'intent'],
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.ConversationV1.prototype.updateWorkspace"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.ConversationV1.prototype.</span>updateWorkspace (params, callback)](#apidoc.element.watson-developer-cloud.ConversationV1.prototype.updateWorkspace)
- description and source-code
```javascript
updateWorkspace = function (params, callback) {
  params = params || {};

  const parameters = {
    options: {
      url: '/v1/workspaces/{workspace_id}',
      method: 'POST',
      json: true,
      body: pick(params, ['name', 'language', 'entities', 'intents', 'dialog_nodes', 'metadata', 'description', 'counterexamples
']),
      path: pick(params, ['workspace_id'])
    },
    requiredParams: ['workspace_id'],
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.ConversationV1.prototype.workspaceStatus"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.ConversationV1.prototype.</span>workspaceStatus (params, callback)](#apidoc.element.watson-developer-cloud.ConversationV1.prototype.workspaceStatus)
- description and source-code
```javascript
workspaceStatus = function (params, callback) {
  params = params || {};

  const parameters = {
    options: {
      url: '/v1/workspaces/{workspace_id}/status',
      method: 'GET',
      json: true,
      path: pick(params, ['workspace_id'])
    },
    requiredParams: ['workspace_id'],
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.watson-developer-cloud.ConversationV1Experimental"></a>[module watson-developer-cloud.ConversationV1Experimental](#apidoc.module.watson-developer-cloud.ConversationV1Experimental)

#### <a name="apidoc.element.watson-developer-cloud.ConversationV1Experimental.ConversationV1Experimental"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.</span>ConversationV1Experimental (options)](#apidoc.element.watson-developer-cloud.ConversationV1Experimental.ConversationV1Experimental)
- description and source-code
```javascript
function ConversationV1Experimental(options) {
  BaseService.call(this, options);

  if (!this._options.silent) {
    // eslint-disable-next-line no-console
    console.warn(
      new Error('Watson Conversation v1-experimental is sunset as of 2016-08-01. Please upgrade to v1. Set {silent: true} to disable
 this message.').stack
    );
  }

  // Check if 'version_date' was provided
  if (typeof this._options.version_date === 'undefined') {
    throw new Error('Argument error: version_date was not specified, use 2016-05-19');
  }
  this._options.qs.version = options.version_date;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.ConversationV1Experimental.super_"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.ConversationV1Experimental.</span>super_ (user_options)](#apidoc.element.watson-developer-cloud.ConversationV1Experimental.super_)
- description and source-code
```javascript
function BaseService(user_options) {
  if (!(this instanceof BaseService)) {
    // it might be better to just create a new instance and return that.. but that can't be done here, it has to be done in each
 individual service. So this is still a good failsafe even in that case.
    throw new Error('"new" keyword required to create Watson service instances');
  }
  let options = extend({}, user_options);

  options = this.initCredentials(options);

  if (options.url) {
    options.url = helper.stripTrailingSlash(options.url);
  }

  this._options = extend({ qs: {}, url: this.constructor.URL }, this.serviceDefaults, options);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.watson-developer-cloud.ConversationV1Experimental.prototype"></a>[module watson-developer-cloud.ConversationV1Experimental.prototype](#apidoc.module.watson-developer-cloud.ConversationV1Experimental.prototype)

#### <a name="apidoc.element.watson-developer-cloud.ConversationV1Experimental.prototype.message"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.ConversationV1Experimental.prototype.</span>message (params, callback)](#apidoc.element.watson-developer-cloud.ConversationV1Experimental.prototype.message)
- description and source-code
```javascript
message = function (params, callback) {
  params = params || {};

  const parameters = {
    options: {
      url: '/v1/workspaces/{workspace_id}/message',
      method: 'POST',
      json: true,
      body: pick(params, ['input', 'context']),
      path: pick(params, ['workspace_id'])
    },
    requiredParams: ['workspace_id'],
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
...

var conversation = new ConversationV1({
 username: '<username>',
 password: '<password>',
 version_date: ConversationV1.VERSION_DATE_2017_02_03
});

conversation.message({
 input: { text: 'What\'s the weather?' },
 workspace_id: '<workspace id>'
}, function(err, response) {
    if (err) {
      console.error(err);
    } else {
      console.log(JSON.stringify(response, null, 2));
...
```



# <a name="apidoc.module.watson-developer-cloud.DialogV1"></a>[module watson-developer-cloud.DialogV1](#apidoc.module.watson-developer-cloud.DialogV1)

#### <a name="apidoc.element.watson-developer-cloud.DialogV1.DialogV1"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.</span>DialogV1 (options)](#apidoc.element.watson-developer-cloud.DialogV1.DialogV1)
- description and source-code
```javascript
function DialogV1(options) {
  BaseService.call(this, options);

  if (!options.silent) {
    // eslint-disable-next-line no-console
    console.warn(
      'WARNING: The Dialog service was deprecated, existing instances of the service will continue to function until August 9, 2017
. See https://www.ibm.com/watson/developercloud/doc/conversation/migration.shtml. Set {silent: true} to disable this message.'
    );
  }
}
```
- example usage
```shell
...
By default, the library tries to use Basic Auth and will ask for 'api_key' or 'username' and 'password' and send an 'Authorization
: Basic XXXXXXX'. You can avoid this by using:

'use_unauthenticated'.

'''javascript
var watson = require('watson-developer-cloud');

var dialog = new watson.DialogV1({
  use_unauthenticated: true
});
'''

## Debug
This library relies on the 'request' npm module writted by
[request][request_github] to call the Watson Services. To debug the apps, add
...
```

#### <a name="apidoc.element.watson-developer-cloud.DialogV1.super_"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.DialogV1.</span>super_ (user_options)](#apidoc.element.watson-developer-cloud.DialogV1.super_)
- description and source-code
```javascript
function BaseService(user_options) {
  if (!(this instanceof BaseService)) {
    // it might be better to just create a new instance and return that.. but that can't be done here, it has to be done in each
 individual service. So this is still a good failsafe even in that case.
    throw new Error('"new" keyword required to create Watson service instances');
  }
  let options = extend({}, user_options);

  options = this.initCredentials(options);

  if (options.url) {
    options.url = helper.stripTrailingSlash(options.url);
  }

  this._options = extend({ qs: {}, url: this.constructor.URL }, this.serviceDefaults, options);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.watson-developer-cloud.DialogV1.prototype"></a>[module watson-developer-cloud.DialogV1.prototype](#apidoc.module.watson-developer-cloud.DialogV1.prototype)

#### <a name="apidoc.element.watson-developer-cloud.DialogV1.prototype.conversation"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.DialogV1.prototype.</span>conversation (params, callback)](#apidoc.element.watson-developer-cloud.DialogV1.prototype.conversation)
- description and source-code
```javascript
conversation = function (params, callback) {
  params = params || {};

  const parameters = {
    options: {
      url: '/v1/dialogs/{dialog_id}/conversation',
      method: 'POST',
      json: true,
      form: omit(params, ['dialog_id']),
      path: params
    },
    requiredParams: ['dialog_id'],
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.DialogV1.prototype.createDialog"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.DialogV1.prototype.</span>createDialog (params, callback)](#apidoc.element.watson-developer-cloud.DialogV1.prototype.createDialog)
- description and source-code
```javascript
createDialog = function (params, callback) {
  params = params || {};

  if (!params.file) {
    callback(new Error('Missing required parameters: file'));
    return;
  }

  if (!isStream(params.file)) {
    callback(new Error('file is not a standard Node.js Stream'));
    return;
  }

  const parameters = {
    options: {
      url: '/v1/dialogs',
      method: 'POST',
      json: true,
      formData: pick(params, ['name', 'file'])
    },
    requiredParams: ['name'],
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.DialogV1.prototype.deleteDialog"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.DialogV1.prototype.</span>deleteDialog (params, callback)](#apidoc.element.watson-developer-cloud.DialogV1.prototype.deleteDialog)
- description and source-code
```javascript
deleteDialog = function (params, callback) {
  const parameters = {
    options: {
      url: '/v1/dialogs/{dialog_id}',
      method: 'DELETE',
      json: true,
      path: params
    },
    requiredParams: ['dialog_id'],
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.DialogV1.prototype.getContent"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.DialogV1.prototype.</span>getContent (params, callback)](#apidoc.element.watson-developer-cloud.DialogV1.prototype.getContent)
- description and source-code
```javascript
getContent = function (params, callback) {
  params = params || {};

  const parameters = {
    options: {
      url: '/v1/dialogs/{dialog_id}/content',
      method: 'GET',
      json: true,
      path: params
    },
    requiredParams: ['dialog_id'],
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.DialogV1.prototype.getConversation"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.DialogV1.prototype.</span>getConversation (params, callback)](#apidoc.element.watson-developer-cloud.DialogV1.prototype.getConversation)
- description and source-code
```javascript
getConversation = function (params, callback) {
  params = params || {};

  const parameters = {
    options: {
      url: '/v1/dialogs/{dialog_id}/conversation',
      method: 'GET',
      json: true,
      qs: omit(params, ['dialog_id']),
      path: params
    },
    requiredParams: ['dialog_id', 'date_from', 'date_to'],
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.DialogV1.prototype.getDialogs"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.DialogV1.prototype.</span>getDialogs (params, callback)](#apidoc.element.watson-developer-cloud.DialogV1.prototype.getDialogs)
- description and source-code
```javascript
getDialogs = function (params, callback) {
  const parameters = {
    options: {
      url: '/v1/dialogs',
      method: 'GET',
      json: true
    },
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.DialogV1.prototype.getProfile"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.DialogV1.prototype.</span>getProfile (params, callback)](#apidoc.element.watson-developer-cloud.DialogV1.prototype.getProfile)
- description and source-code
```javascript
getProfile = function (params, callback) {
  params = params || {};

  const parameters = {
    options: {
      url: '/v1/dialogs/{dialog_id}/profile',
      method: 'GET',
      json: true,
      path: params,
      qs: pick(params, ['client_id', 'name'])
    },
    requiredParams: ['dialog_id', 'client_id'],
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.DialogV1.prototype.updateContent"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.DialogV1.prototype.</span>updateContent (params, callback)](#apidoc.element.watson-developer-cloud.DialogV1.prototype.updateContent)
- description and source-code
```javascript
updateContent = function (params, callback) {
  params = params || {};

  const parameters = {
    options: {
      url: '/v1/dialogs/{dialog_id}/content',
      method: 'PUT',
      json: true,
      path: params
    },
    requiredParams: ['dialog_id'],
    defaultOptions: extend(true, {}, this._options, pick(params, ['headers']))
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.DialogV1.prototype.updateDialog"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.DialogV1.prototype.</span>updateDialog (params, callback)](#apidoc.element.watson-developer-cloud.DialogV1.prototype.updateDialog)
- description and source-code
```javascript
updateDialog = function (params, callback) {
  params = params || {};

  if (!params.file) {
    callback(new Error('Missing required parameters: file'));
    return;
  }

  if (!isStream(params.file)) {
    callback(new Error('file is not a standard Node.js Stream'));
    return;
  }

  const parameters = {
    options: {
      url: '/v1/dialogs/{dialog_id}',
      method: 'PUT',
      json: true,
      path: params,
      formData: omit(params, ['dialog_id'])
    },
    requiredParams: ['dialog_id'],
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.DialogV1.prototype.updateProfile"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.DialogV1.prototype.</span>updateProfile (params, callback)](#apidoc.element.watson-developer-cloud.DialogV1.prototype.updateProfile)
- description and source-code
```javascript
updateProfile = function (params, callback) {
  params = params || {};

  const parameters = {
    options: {
      url: '/v1/dialogs/{dialog_id}/profile',
      method: 'PUT',
      json: true,
      body: pick(params, ['name_values', 'client_id']),
      path: params
    },
    requiredParams: ['dialog_id', 'name_values'],
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.watson-developer-cloud.DiscoveryV1"></a>[module watson-developer-cloud.DiscoveryV1](#apidoc.module.watson-developer-cloud.DiscoveryV1)

#### <a name="apidoc.element.watson-developer-cloud.DiscoveryV1.DiscoveryV1"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.</span>DiscoveryV1 (options)](#apidoc.element.watson-developer-cloud.DiscoveryV1.DiscoveryV1)
- description and source-code
```javascript
function DiscoveryV1(options) {
  BaseService.call(this, options);

  // Check if 'version_date' was provided
  if (typeof this._options.version_date === 'undefined') {
    throw new Error('Argument error: version_date was not specified, use DiscoveryV1.VERSION_DATE_2016_12_15');
  }
  this._options.qs.version = options.version_date;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.DiscoveryV1.super_"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.DiscoveryV1.</span>super_ (user_options)](#apidoc.element.watson-developer-cloud.DiscoveryV1.super_)
- description and source-code
```javascript
function BaseService(user_options) {
  if (!(this instanceof BaseService)) {
    // it might be better to just create a new instance and return that.. but that can't be done here, it has to be done in each
 individual service. So this is still a good failsafe even in that case.
    throw new Error('"new" keyword required to create Watson service instances');
  }
  let options = extend({}, user_options);

  options = this.initCredentials(options);

  if (options.url) {
    options.url = helper.stripTrailingSlash(options.url);
  }

  this._options = extend({ qs: {}, url: this.constructor.URL }, this.serviceDefaults, options);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.watson-developer-cloud.DiscoveryV1.prototype"></a>[module watson-developer-cloud.DiscoveryV1.prototype](#apidoc.module.watson-developer-cloud.DiscoveryV1.prototype)

#### <a name="apidoc.element.watson-developer-cloud.DiscoveryV1.prototype.addDocument"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.DiscoveryV1.prototype.</span>addDocument (params, callback)](#apidoc.element.watson-developer-cloud.DiscoveryV1.prototype.addDocument)
- description and source-code
```javascript
addDocument = function (params, callback) {
  params = params || {};

  const queryParams = pick(params, ['configuration_id']);
  const formDataParams = pick(params, ['file', 'metadata']);

  // if we get a buffer or object, we need to include stuff about filename for the service
  if (formDataParams.file) {
    if (
      typeof formDataParams.file.filename !== 'string' &&
      !(formDataParams.file.options && typeof formDataParams.file.options.filename !== 'string') &&
      !(formDataParams.file.path && typeof formDataParams.file.path !== 'string') &&
      !(formDataParams.file.name && typeof formDataParams.file.name !== 'string')
    ) {
      const filedat = formDataParams.file;
      // the filename used below is because the name must exist
      formDataParams.file = { value: filedat, options: { filename: '_' } };
    }
  }

  const parameters = {
    options: {
      url: '/v1/environments/{environment_id}/collections/{collection_id}/documents',
      method: 'POST',
      path: pick(params, ['environment_id', 'collection_id']),
      qs: queryParams,
      formData: formDataParams,
      json: true
    },
    requiredParams: ['environment_id', 'collection_id', 'file'],
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.DiscoveryV1.prototype.createCollection"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.DiscoveryV1.prototype.</span>createCollection (params, callback)](#apidoc.element.watson-developer-cloud.DiscoveryV1.prototype.createCollection)
- description and source-code
```javascript
createCollection = function (params, callback) {
  params = params || {};

  params.language_code = params.language_code || 'en_us';

  const parameters = {
    options: {
      url: '/v1/environments/{environment_id}/collections',
      method: 'POST',
      path: pick(params, ['environment_id']),
      multipart: [
        {
          'content-type': 'application/json',
          body: JSON.stringify(pick(params, ['collection_name', 'description', 'configuration_id', 'language_code']))
        }
      ],
      json: true
    },
    originalParams: params,
    requiredParams: ['environment_id', 'configuration_id', 'collection_name'],
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.DiscoveryV1.prototype.createEnvironment"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.DiscoveryV1.prototype.</span>createEnvironment (params, callback)](#apidoc.element.watson-developer-cloud.DiscoveryV1.prototype.createEnvironment)
- description and source-code
```javascript
createEnvironment = function (params, callback) {
  params = params || {};

  // size is an int of 1,2,3, default 1
  if (!params.size) {
    params.size = 1;
  }

  const parameters = {
    options: {
      url: '/v1/environments',
      method: 'POST',
      multipart: [
        {
          'content-type': 'application/json',
          body: JSON.stringify(pick(params, ['name', 'description', 'size']))
        }
      ],
      json: true
    },
    originalParams: params,
    requiredParams: ['name', 'description'],
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.DiscoveryV1.prototype.deleteCollection"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.DiscoveryV1.prototype.</span>deleteCollection (params, callback)](#apidoc.element.watson-developer-cloud.DiscoveryV1.prototype.deleteCollection)
- description and source-code
```javascript
deleteCollection = function (params, callback) {
  params = params || {};

  params.language_code = params.language_code || 'en_us';

  const parameters = {
    options: {
      url: '/v1/environments/{environment_id}/collections/{collection_id}',
      method: 'DELETE',
      path: pick(params, ['environment_id', 'collection_id']),
      json: true
    },
    requiredParams: ['environment_id', 'collection_id'],
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.DiscoveryV1.prototype.deleteDocument"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.DiscoveryV1.prototype.</span>deleteDocument (params, callback)](#apidoc.element.watson-developer-cloud.DiscoveryV1.prototype.deleteDocument)
- description and source-code
```javascript
deleteDocument = function (params, callback) {
  params = params || {};

  const parameters = {
    options: {
      url: '/v1/environments/{environment_id}/collections/{collection_id}/documents/{document_id}',
      method: 'DELETE',
      path: pick(params, ['environment_id', 'collection_id', 'document_id']),
      json: true
    },
    requiredParams: ['environment_id', 'collection_id', 'document_id'],
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.DiscoveryV1.prototype.deleteEnvironment"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.DiscoveryV1.prototype.</span>deleteEnvironment (params, callback)](#apidoc.element.watson-developer-cloud.DiscoveryV1.prototype.deleteEnvironment)
- description and source-code
```javascript
deleteEnvironment = function (params, callback) {
  params = params || {};

  const parameters = {
    options: {
      url: '/v1/environments/{environment_id}',
      method: 'DELETE',
      path: pick(params, ['environment_id']),
      json: true
    },
    requiredParams: ['environment_id'],
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.DiscoveryV1.prototype.getCollection"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.DiscoveryV1.prototype.</span>getCollection (params, callback)](#apidoc.element.watson-developer-cloud.DiscoveryV1.prototype.getCollection)
- description and source-code
```javascript
getCollection = function (params, callback) {
  params = params || {};

  const parameters = {
    options: {
      url: '/v1/environments/{environment_id}/collections/{collection_id}',
      method: 'GET',
      path: pick(params, ['environment_id', 'collection_id']),
      json: true
    },
    requiredParams: ['environment_id', 'collection_id'],
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.DiscoveryV1.prototype.getCollections"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.DiscoveryV1.prototype.</span>getCollections (params, callback)](#apidoc.element.watson-developer-cloud.DiscoveryV1.prototype.getCollections)
- description and source-code
```javascript
getCollections = function (params, callback) {
  params = params || {};

  const parameters = {
    options: {
      url: '/v1/environments/{environment_id}/collections',
      method: 'GET',
      path: pick(params, ['environment_id']),
      json: true
    },
    requiredParams: ['environment_id'],
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.DiscoveryV1.prototype.getConfiguration"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.DiscoveryV1.prototype.</span>getConfiguration (params, callback)](#apidoc.element.watson-developer-cloud.DiscoveryV1.prototype.getConfiguration)
- description and source-code
```javascript
getConfiguration = function (params, callback) {
  params = params || {};

  const parameters = {
    options: {
      url: '/v1/environments/{environment_id}/configurations/{configuration_id}',
      method: 'GET',
      path: pick(params, ['environment_id', 'configuration_id']),
      json: true
    },
    requiredParams: ['environment_id', 'configuration_id'],
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.DiscoveryV1.prototype.getConfigurations"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.DiscoveryV1.prototype.</span>getConfigurations (params, callback)](#apidoc.element.watson-developer-cloud.DiscoveryV1.prototype.getConfigurations)
- description and source-code
```javascript
getConfigurations = function (params, callback) {
  params = params || {};

  const parameters = {
    options: {
      url: '/v1/environments/{environment_id}/configurations',
      method: 'GET',
      path: pick(params, ['environment_id']),
      json: true
    },
    requiredParams: ['environment_id'],
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.DiscoveryV1.prototype.getEnvironment"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.DiscoveryV1.prototype.</span>getEnvironment (params, callback)](#apidoc.element.watson-developer-cloud.DiscoveryV1.prototype.getEnvironment)
- description and source-code
```javascript
getEnvironment = function (params, callback) {
  params = params || {};

  const parameters = {
    options: {
      url: '/v1/environments/{environment_id}',
      method: 'GET',
      path: pick(params, ['environment_id']),
      json: true
    },
    requiredParams: ['environment_id'],
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.DiscoveryV1.prototype.getEnvironments"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.DiscoveryV1.prototype.</span>getEnvironments (params, callback)](#apidoc.element.watson-developer-cloud.DiscoveryV1.prototype.getEnvironments)
- description and source-code
```javascript
getEnvironments = function (params, callback) {
  params = params || {};

  const parameters = {
    options: {
      url: '/v1/environments',
      method: 'GET',
      json: true
    },
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.DiscoveryV1.prototype.query"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.DiscoveryV1.prototype.</span>query (params, callback)](#apidoc.element.watson-developer-cloud.DiscoveryV1.prototype.query)
- description and source-code
```javascript
query = function (params, callback) {
  params = params || {};

  const parameters = {
    options: {
      url: '/v1/environments/{environment_id}/collections/{collection_id}/query',
      method: 'GET',
      json: true,
      path: pick(params, ['environment_id', 'collection_id']),
      qs: pick(params, ['filter', 'aggregation', 'return', 'count', 'offset', 'query'])
    },
    requiredParams: ['environment_id', 'collection_id'],
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
...

var discovery = new DiscoveryV1({
username: '<username>',
password: '<password>',
version_date: DiscoveryV1.VERSION_DATE_2016_12_15
});

discovery.query({
  environment_id: '<environment_id>',
  collection_id: '<collection_id>',
  query:
}, function(err, response) {
      if (err) {
        console.error(err);
      } else {
...
```

#### <a name="apidoc.element.watson-developer-cloud.DiscoveryV1.prototype.updateDocument"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.DiscoveryV1.prototype.</span>updateDocument (params, callback)](#apidoc.element.watson-developer-cloud.DiscoveryV1.prototype.updateDocument)
- description and source-code
```javascript
updateDocument = function (params, callback) {
  params = params || {};

  const queryParams = pick(params, ['configuration_id']);
  const formDataParams = pick(params, ['file', 'metadata']);

  // if we get a buffer or object, we need to include stuff about filename for the service
  if (formDataParams.file) {
    if (
      typeof formDataParams.file.filename !== 'string' &&
      !(formDataParams.file.options && typeof formDataParams.file.options.filename !== 'string') &&
      !(formDataParams.file.path && typeof formDataParams.file.path !== 'string') &&
      !(formDataParams.file.name && typeof formDataParams.file.name !== 'string')
    ) {
      const filedat = formDataParams.file;
      // the filename used below is because the name must exist
      formDataParams.file = { value: filedat, options: { filename: '_' } };
    }
  }

  const parameters = {
    options: {
      url: '/v1/environments/{environment_id}/collections/{collection_id}/documents/{document_id}',
      method: 'POST',
      path: pick(params, ['environment_id', 'collection_id', 'document_id']),
      qs: queryParams,
      formData: formDataParams,
      json: true
    },
    requiredParams: ['environment_id', 'collection_id', 'document_id', 'file'],
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.watson-developer-cloud.DiscoveryV1Experimental"></a>[module watson-developer-cloud.DiscoveryV1Experimental](#apidoc.module.watson-developer-cloud.DiscoveryV1Experimental)

#### <a name="apidoc.element.watson-developer-cloud.DiscoveryV1Experimental.DiscoveryV1Experimental"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.</span>DiscoveryV1Experimental (options)](#apidoc.element.watson-developer-cloud.DiscoveryV1Experimental.DiscoveryV1Experimental)
- description and source-code
```javascript
function DiscoveryV1Experimental(options) {
  BaseService.call(this, options);

  // Check if 'version_date' was provided
  if (typeof this._options.version_date === 'undefined') {
    throw new Error('Argument error: version_date was not specified, use DiscoveryV1Experimental.VERSION_DATE_2016_07_11');
  }
  this._options.qs.version = options.version_date;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.DiscoveryV1Experimental.super_"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.DiscoveryV1Experimental.</span>super_ (user_options)](#apidoc.element.watson-developer-cloud.DiscoveryV1Experimental.super_)
- description and source-code
```javascript
function BaseService(user_options) {
  if (!(this instanceof BaseService)) {
    // it might be better to just create a new instance and return that.. but that can't be done here, it has to be done in each
 individual service. So this is still a good failsafe even in that case.
    throw new Error('"new" keyword required to create Watson service instances');
  }
  let options = extend({}, user_options);

  options = this.initCredentials(options);

  if (options.url) {
    options.url = helper.stripTrailingSlash(options.url);
  }

  this._options = extend({ qs: {}, url: this.constructor.URL }, this.serviceDefaults, options);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.watson-developer-cloud.DiscoveryV1Experimental.prototype"></a>[module watson-developer-cloud.DiscoveryV1Experimental.prototype](#apidoc.module.watson-developer-cloud.DiscoveryV1Experimental.prototype)

#### <a name="apidoc.element.watson-developer-cloud.DiscoveryV1Experimental.prototype.getCollection"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.DiscoveryV1Experimental.prototype.</span>getCollection (params, collectionId, callback)](#apidoc.element.watson-developer-cloud.DiscoveryV1Experimental.prototype.getCollection)
- description and source-code
```javascript
getCollection = function (params, collectionId, callback) {
  params = params || {};

  const parameters = {
    options: {
      url: '/v1/environments/{environment_id}/collections/{collection_id}',
      method: 'GET',
      path: pick(params, ['environment_id', 'collection_id']),
      json: true
    },
    requiredParams: ['environment_id', 'collection_id'],
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.DiscoveryV1Experimental.prototype.getCollections"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.DiscoveryV1Experimental.prototype.</span>getCollections (params, callback)](#apidoc.element.watson-developer-cloud.DiscoveryV1Experimental.prototype.getCollections)
- description and source-code
```javascript
getCollections = function (params, callback) {
  params = params || {};

  const parameters = {
    options: {
      url: '/v1/environments/{environment_id}/collections',
      method: 'GET',
      path: pick(params, ['environment_id']),
      json: true
    },
    requiredParams: ['environment_id'],
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.DiscoveryV1Experimental.prototype.getEnvironment"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.DiscoveryV1Experimental.prototype.</span>getEnvironment (params, callback)](#apidoc.element.watson-developer-cloud.DiscoveryV1Experimental.prototype.getEnvironment)
- description and source-code
```javascript
getEnvironment = function (params, callback) {
  params = params || {};

  const parameters = {
    options: {
      url: '/v1/environments/{environment_id}',
      method: 'GET',
      path: pick(params, ['environment_id']),
      json: true
    },
    requiredParams: ['environment_id'],
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.DiscoveryV1Experimental.prototype.getEnvironments"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.DiscoveryV1Experimental.prototype.</span>getEnvironments (params, callback)](#apidoc.element.watson-developer-cloud.DiscoveryV1Experimental.prototype.getEnvironments)
- description and source-code
```javascript
getEnvironments = function (params, callback) {
  params = params || {};

  const parameters = {
    options: {
      url: '/v1/environments',
      method: 'GET',
      json: true,
      qs: pick(params, ['name'])
    },
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.DiscoveryV1Experimental.prototype.query"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.DiscoveryV1Experimental.prototype.</span>query (params, callback)](#apidoc.element.watson-developer-cloud.DiscoveryV1Experimental.prototype.query)
- description and source-code
```javascript
query = function (params, callback) {
  params = params || {};

  const parameters = {
    options: {
      url: '/v1/environments/{environment_id}/collections/{collection_id}/query',
      method: 'GET',
      json: true,
      path: pick(params, ['environment_id', 'collection_id']),
      qs: pick(params, ['filter', 'aggregation', 'return', 'count', 'offset', 'query'])
    },
    requiredParams: ['environment_id', 'collection_id'],
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
...

var discovery = new DiscoveryV1({
username: '<username>',
password: '<password>',
version_date: DiscoveryV1.VERSION_DATE_2016_12_15
});

discovery.query({
  environment_id: '<environment_id>',
  collection_id: '<collection_id>',
  query:
}, function(err, response) {
      if (err) {
        console.error(err);
      } else {
...
```



# <a name="apidoc.module.watson-developer-cloud.DocumentConversionV1"></a>[module watson-developer-cloud.DocumentConversionV1](#apidoc.module.watson-developer-cloud.DocumentConversionV1)

#### <a name="apidoc.element.watson-developer-cloud.DocumentConversionV1.DocumentConversionV1"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.</span>DocumentConversionV1 (options)](#apidoc.element.watson-developer-cloud.DocumentConversionV1.DocumentConversionV1)
- description and source-code
```javascript
function DocumentConversionV1(options) {
  BaseService.call(this, options);

  // Warn if not specifying version date
  if (!this._options.version_date && !this._options.silent) {
    // eslint-disable-next-line no-console
    console.warn(
      '[DocumentConversion] WARNING: No version_date specified. Using a (possibly old) default. ' +
        'e.g. watson.document_conversion({ version_date: "2015-12-15" })'
    );
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.DocumentConversionV1.super_"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.DocumentConversionV1.</span>super_ (user_options)](#apidoc.element.watson-developer-cloud.DocumentConversionV1.super_)
- description and source-code
```javascript
function BaseService(user_options) {
  if (!(this instanceof BaseService)) {
    // it might be better to just create a new instance and return that.. but that can't be done here, it has to be done in each
 individual service. So this is still a good failsafe even in that case.
    throw new Error('"new" keyword required to create Watson service instances');
  }
  let options = extend({}, user_options);

  options = this.initCredentials(options);

  if (options.url) {
    options.url = helper.stripTrailingSlash(options.url);
  }

  this._options = extend({ qs: {}, url: this.constructor.URL }, this.serviceDefaults, options);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.watson-developer-cloud.DocumentConversionV1.prototype"></a>[module watson-developer-cloud.DocumentConversionV1.prototype](#apidoc.module.watson-developer-cloud.DocumentConversionV1.prototype)

#### <a name="apidoc.element.watson-developer-cloud.DocumentConversionV1.prototype.addDocumentToBatch"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.DocumentConversionV1.prototype.</span>addDocumentToBatch ()](#apidoc.element.watson-developer-cloud.DocumentConversionV1.prototype.addDocumentToBatch)
- description and source-code
```javascript
function deprecated() {
  throw new Error('The DocumentConversion.' + name + '() method was deprecated and is no longer available, please use convert()
instead.');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.DocumentConversionV1.prototype.convert"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.DocumentConversionV1.prototype.</span>convert (params, callback)](#apidoc.element.watson-developer-cloud.DocumentConversionV1.prototype.convert)
- description and source-code
```javascript
convert = function (params, callback) {
  params = params || {};
  if (typeof params.conversion_target === 'string') {
    params.conversion_target = params.conversion_target.toLowerCase();
  }
  const keys = Object.keys(DocumentConversionV1.prototype.conversion_target);
  const values = keys.map(function(v) {
    return DocumentConversionV1.prototype.conversion_target[v];
  });
  if (values.indexOf(params.conversion_target) === -1) {
    callback(new Error('Missing required parameters: conversion_target. Possible values are: ' + values.join(', ')));
    return;
  }

  if (!params.file && !params.document_id) {
    callback(new Error('Missing required parameters: either params.file or params.document_id must be specified'));
    return;
  }

  if (params.file && !isStream(params.file) && !Buffer.isBuffer(params.file) && !params.file.value) {
    callback(new Error('Missing required parameters: file is not a standard Node.js Stream or Buffer'));
    return;
  }

  const parameters = {
    options: {
      method: 'POST',
      url: '/v1/convert_document',
      json: true
    },
    defaultOptions: this._options
  };

  // send the parameters in the body or as formData depending on the request
  if (params.file) {
    fixupContentType(params);
    parameters.options.formData = {
      file: params.file,
      config: {
        value: JSON.stringify(params.config || omit(params, ['file', 'content_type'])),
        options: {
          contentType: 'application/json; charset=utf-8'
        }
      }
    };
  } else {
    parameters.options.body = params;
  }

  return requestFactory(parameters, callback);
}
```
- example usage
```shell
...
var document_conversion = new DocumentConversionV1({
username:     '<username>',
password:     '<password>',
version_date: '2015-12-01'
});

// convert a single document
document_conversion.convert({
// (JSON) ANSWER_UNITS, NORMALIZED_HTML, or NORMALIZED_TEXT
file: fs.createReadStream('sample-docx.docx'),
conversion_target: document_conversion.conversion_target.ANSWER_UNITS,
// Add custom configuration properties or omit for defaults
word: {
  heading: {
    fonts: [
...
```

#### <a name="apidoc.element.watson-developer-cloud.DocumentConversionV1.prototype.createBatch"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.DocumentConversionV1.prototype.</span>createBatch ()](#apidoc.element.watson-developer-cloud.DocumentConversionV1.prototype.createBatch)
- description and source-code
```javascript
function deprecated() {
  throw new Error('The DocumentConversion.' + name + '() method was deprecated and is no longer available, please use convert()
instead.');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.DocumentConversionV1.prototype.createJob"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.DocumentConversionV1.prototype.</span>createJob ()](#apidoc.element.watson-developer-cloud.DocumentConversionV1.prototype.createJob)
- description and source-code
```javascript
function deprecated() {
  throw new Error('The DocumentConversion.' + name + '() method was deprecated and is no longer available, please use convert()
instead.');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.DocumentConversionV1.prototype.getBatch"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.DocumentConversionV1.prototype.</span>getBatch ()](#apidoc.element.watson-developer-cloud.DocumentConversionV1.prototype.getBatch)
- description and source-code
```javascript
function deprecated() {
  throw new Error('The DocumentConversion.' + name + '() method was deprecated and is no longer available, please use convert()
instead.');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.DocumentConversionV1.prototype.getBatchDocument"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.DocumentConversionV1.prototype.</span>getBatchDocument ()](#apidoc.element.watson-developer-cloud.DocumentConversionV1.prototype.getBatchDocument)
- description and source-code
```javascript
function deprecated() {
  throw new Error('The DocumentConversion.' + name + '() method was deprecated and is no longer available, please use convert()
instead.');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.DocumentConversionV1.prototype.getBatchDocuments"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.DocumentConversionV1.prototype.</span>getBatchDocuments ()](#apidoc.element.watson-developer-cloud.DocumentConversionV1.prototype.getBatchDocuments)
- description and source-code
```javascript
function deprecated() {
  throw new Error('The DocumentConversion.' + name + '() method was deprecated and is no longer available, please use convert()
instead.');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.DocumentConversionV1.prototype.getBatches"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.DocumentConversionV1.prototype.</span>getBatches ()](#apidoc.element.watson-developer-cloud.DocumentConversionV1.prototype.getBatches)
- description and source-code
```javascript
function deprecated() {
  throw new Error('The DocumentConversion.' + name + '() method was deprecated and is no longer available, please use convert()
instead.');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.DocumentConversionV1.prototype.getDocument"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.DocumentConversionV1.prototype.</span>getDocument ()](#apidoc.element.watson-developer-cloud.DocumentConversionV1.prototype.getDocument)
- description and source-code
```javascript
function deprecated() {
  throw new Error('The DocumentConversion.' + name + '() method was deprecated and is no longer available, please use convert()
instead.');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.DocumentConversionV1.prototype.getDocuments"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.DocumentConversionV1.prototype.</span>getDocuments ()](#apidoc.element.watson-developer-cloud.DocumentConversionV1.prototype.getDocuments)
- description and source-code
```javascript
function deprecated() {
  throw new Error('The DocumentConversion.' + name + '() method was deprecated and is no longer available, please use convert()
instead.');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.DocumentConversionV1.prototype.getJob"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.DocumentConversionV1.prototype.</span>getJob ()](#apidoc.element.watson-developer-cloud.DocumentConversionV1.prototype.getJob)
- description and source-code
```javascript
function deprecated() {
  throw new Error('The DocumentConversion.' + name + '() method was deprecated and is no longer available, please use convert()
instead.');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.DocumentConversionV1.prototype.getJobLog"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.DocumentConversionV1.prototype.</span>getJobLog ()](#apidoc.element.watson-developer-cloud.DocumentConversionV1.prototype.getJobLog)
- description and source-code
```javascript
function deprecated() {
  throw new Error('The DocumentConversion.' + name + '() method was deprecated and is no longer available, please use convert()
instead.');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.DocumentConversionV1.prototype.getJobs"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.DocumentConversionV1.prototype.</span>getJobs ()](#apidoc.element.watson-developer-cloud.DocumentConversionV1.prototype.getJobs)
- description and source-code
```javascript
function deprecated() {
  throw new Error('The DocumentConversion.' + name + '() method was deprecated and is no longer available, please use convert()
instead.');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.DocumentConversionV1.prototype.getOutput"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.DocumentConversionV1.prototype.</span>getOutput ()](#apidoc.element.watson-developer-cloud.DocumentConversionV1.prototype.getOutput)
- description and source-code
```javascript
function deprecated() {
  throw new Error('The DocumentConversion.' + name + '() method was deprecated and is no longer available, please use convert()
instead.');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.DocumentConversionV1.prototype.getOutputs"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.DocumentConversionV1.prototype.</span>getOutputs ()](#apidoc.element.watson-developer-cloud.DocumentConversionV1.prototype.getOutputs)
- description and source-code
```javascript
function deprecated() {
  throw new Error('The DocumentConversion.' + name + '() method was deprecated and is no longer available, please use convert()
instead.');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.DocumentConversionV1.prototype.index"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.DocumentConversionV1.prototype.</span>index (params, callback)](#apidoc.element.watson-developer-cloud.DocumentConversionV1.prototype.index)
- description and source-code
```javascript
index = function (params, callback) {
  params = params || {};
  if (!params.file && !params.metadata) {
    callback(new Error('Missing required parameters: file or metadata. At least one of those is required.'));
    return;
  }
  if (params.file && !isStream(params.file) && !Buffer.isBuffer(params.file) && !params.file.value) {
    callback(new Error('Missing required parameters: file is not a standard Node.js Stream or Buffer'));
    return;
  }
  if (!params.config) {
    callback(new Error('Missing required parameters: file or metadata. At least one of those is required.'));
    return;
  }

  const parameters = {
    options: {
      method: 'POST',
      url: '/v1/index_document',
      json: true
    },
    defaultOptions: this._options
  };

  // send the parameters as formData
  if (params.file && params.metadata) {
    fixupContentType(params);
    parameters.options.formData = {
      file: params.file,
      config: {
        value: JSON.stringify(params.config),
        options: {
          contentType: 'application/json; charset=utf-8'
        }
      },
      metadata: {
        value: JSON.stringify(params.metadata),
        options: {
          contentType: 'application/json; charset=utf-8'
        }
      }
    };
  } else if (params.file) {
    fixupContentType(params);
    parameters.options.formData = {
      file: params.file,
      config: {
        value: JSON.stringify(params.config),
        options: {
          contentType: 'application/json; charset=utf-8'
        }
      }
    };
  } else if (params.metadata) {
    parameters.options.formData = {
      config: {
        value: JSON.stringify(params.config),
        options: {
          contentType: 'application/json; charset=utf-8'
        }
      },
      metadata: {
        value: JSON.stringify(params.metadata),
        options: {
          contentType: 'application/json; charset=utf-8'
        }
      }
    };
  } else {
    callback(new Error('Missing required parameters: file or metadata. At least one of those is required.'));
    return;
  }

  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.DocumentConversionV1.prototype.updateBatch"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.DocumentConversionV1.prototype.</span>updateBatch ()](#apidoc.element.watson-developer-cloud.DocumentConversionV1.prototype.updateBatch)
- description and source-code
```javascript
function deprecated() {
  throw new Error('The DocumentConversion.' + name + '() method was deprecated and is no longer available, please use convert()
instead.');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.DocumentConversionV1.prototype.uploadDocument"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.DocumentConversionV1.prototype.</span>uploadDocument ()](#apidoc.element.watson-developer-cloud.DocumentConversionV1.prototype.uploadDocument)
- description and source-code
```javascript
function deprecated() {
  throw new Error('The DocumentConversion.' + name + '() method was deprecated and is no longer available, please use convert()
instead.');
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.watson-developer-cloud.LanguageTranslationV2"></a>[module watson-developer-cloud.LanguageTranslationV2](#apidoc.module.watson-developer-cloud.LanguageTranslationV2)

#### <a name="apidoc.element.watson-developer-cloud.LanguageTranslationV2.LanguageTranslationV2"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.</span>LanguageTranslationV2 (options)](#apidoc.element.watson-developer-cloud.LanguageTranslationV2.LanguageTranslationV2)
- description and source-code
```javascript
function LanguageTranslationV2(options) {
  BaseService.call(this, options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.LanguageTranslationV2.super_"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.LanguageTranslationV2.</span>super_ (user_options)](#apidoc.element.watson-developer-cloud.LanguageTranslationV2.super_)
- description and source-code
```javascript
function BaseService(user_options) {
  if (!(this instanceof BaseService)) {
    // it might be better to just create a new instance and return that.. but that can't be done here, it has to be done in each
 individual service. So this is still a good failsafe even in that case.
    throw new Error('"new" keyword required to create Watson service instances');
  }
  let options = extend({}, user_options);

  options = this.initCredentials(options);

  if (options.url) {
    options.url = helper.stripTrailingSlash(options.url);
  }

  this._options = extend({ qs: {}, url: this.constructor.URL }, this.serviceDefaults, options);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.watson-developer-cloud.LanguageTranslationV2.prototype"></a>[module watson-developer-cloud.LanguageTranslationV2.prototype](#apidoc.module.watson-developer-cloud.LanguageTranslationV2.prototype)

#### <a name="apidoc.element.watson-developer-cloud.LanguageTranslationV2.prototype.createModel"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.LanguageTranslationV2.prototype.</span>createModel (params, callback)](#apidoc.element.watson-developer-cloud.LanguageTranslationV2.prototype.createModel)
- description and source-code
```javascript
createModel = function (params, callback) {
  params = params || {};

  const missingParams = helper.getMissingParams(params, ['base_model_id']);
  if (missingParams) {
    callback(missingParams);
    return;
  }

  const inputTypes = ['forced_glossary', 'parallel_corpus', 'monolingual_corpus'];

  for (const type in inputTypes) {
    if (inputTypes.hasOwnProperty(type)) {
      if (params[inputTypes[type]] && !isStream(params[inputTypes[type]])) {
        callback(new Error(inputTypes[type] + ' is not a standard Node.js Stream'));
        return;
      }
    }
  }

  const parameters = {
    options: {
      method: 'POST',
      url: '/v2/models',
      qs: pick(params, ['name', 'base_model_id']),
      formData: pick(params, inputTypes),
      json: true
    },
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.LanguageTranslationV2.prototype.deleteModel"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.LanguageTranslationV2.prototype.</span>deleteModel (params, callback)](#apidoc.element.watson-developer-cloud.LanguageTranslationV2.prototype.deleteModel)
- description and source-code
```javascript
deleteModel = function (params, callback) {
  params = params || {};

  const parameters = {
    options: {
      method: 'DELETE',
      url: '/v2/models/{model_id}',
      path: pick(params, ['model_id']),
      json: true
    },
    requiredParams: ['model_id'],
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.LanguageTranslationV2.prototype.getIdentifiableLanguages"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.LanguageTranslationV2.prototype.</span>getIdentifiableLanguages (params, callback)](#apidoc.element.watson-developer-cloud.LanguageTranslationV2.prototype.getIdentifiableLanguages)
- description and source-code
```javascript
getIdentifiableLanguages = function (params, callback) {
  params = params || {};

  const parameters = {
    options: {
      url: '/v2/identifiable_languages',
      method: 'GET'
    },
    defaultOptions: this._options
  };

  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.LanguageTranslationV2.prototype.getModel"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.LanguageTranslationV2.prototype.</span>getModel (params, callback)](#apidoc.element.watson-developer-cloud.LanguageTranslationV2.prototype.getModel)
- description and source-code
```javascript
getModel = function (params, callback) {
  params = params || {};

  const parameters = {
    options: {
      method: 'GET',
      url: '/v2/models/{model_id}',
      path: pick(params, ['model_id']),
      json: true
    },
    requiredParams: ['model_id'],
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.LanguageTranslationV2.prototype.getModels"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.LanguageTranslationV2.prototype.</span>getModels (params, callback)](#apidoc.element.watson-developer-cloud.LanguageTranslationV2.prototype.getModels)
- description and source-code
```javascript
getModels = function (params, callback) {
  params = params || {};

  const parameters = {
    options: {
      method: 'GET',
      url: '/v2/models',
      qs: pick(params, ['default', 'source', 'target']),
      json: true
    },
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.LanguageTranslationV2.prototype.identify"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.LanguageTranslationV2.prototype.</span>identify (params, callback)](#apidoc.element.watson-developer-cloud.LanguageTranslationV2.prototype.identify)
- description and source-code
```javascript
identify = function (params, callback) {
  if (!params || !params.text) {
    callback(new Error('Missing required parameters: text'));
    return;
  }

  const parameters = {
    options: {
      url: '/v2/identify',
      method: 'POST',
      body: params.text
    },
    defaultOptions: extend(true, {}, this._options, {
      headers: {
        accept: 'application/json',
        'content-type': 'text/plain'
      }
    })
  };

  return requestFactory(parameters, callback);
}
```
- example usage
```shell
...
  function (err, translation) {
    if (err)
      console.log('error:', err);
    else
      console.log(JSON.stringify(translation, null, 2));
});

language_translator.identify({
  text: 'The language translator service takes text input and identifies the language used.' },
  function (err, language) {
    if (err)
      console.log('error:', err);
    else
      console.log(JSON.stringify(language, null, 2));
});
...
```

#### <a name="apidoc.element.watson-developer-cloud.LanguageTranslationV2.prototype.translate"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.LanguageTranslationV2.prototype.</span>translate (params, callback)](#apidoc.element.watson-developer-cloud.LanguageTranslationV2.prototype.translate)
- description and source-code
```javascript
translate = function (params, callback) {
  params = params || {};

  if (!(params.model_id || params.source && params.target)) {
    callback(new Error('Missing required parameters: model_id or source and target'));
    return;
  }
  const parameters = {
    options: {
      url: '/v2/translate',
      method: 'POST',
      json: true,
      body: pick(params, ['source', 'target', 'text', 'model_id'])
    },
    requiredParams: ['text'],
    defaultOptions: this._options
  };

  return requestFactory(parameters, callback);
}
```
- example usage
```shell
...

var language_translator = new LanguageTranslatorV2({
  username: '<username>',
  password: '<password>',
  url: 'https://gateway.watsonplatform.net/language-translator/api/'
});

language_translator.translate({
  text: 'A sentence must have a verb', source : 'en', target: 'es' },
  function (err, translation) {
    if (err)
      console.log('error:', err);
    else
      console.log(JSON.stringify(translation, null, 2));
});
...
```



# <a name="apidoc.module.watson-developer-cloud.LanguageTranslatorV2"></a>[module watson-developer-cloud.LanguageTranslatorV2](#apidoc.module.watson-developer-cloud.LanguageTranslatorV2)

#### <a name="apidoc.element.watson-developer-cloud.LanguageTranslatorV2.LanguageTranslatorV2"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.</span>LanguageTranslatorV2 (options)](#apidoc.element.watson-developer-cloud.LanguageTranslatorV2.LanguageTranslatorV2)
- description and source-code
```javascript
function LanguageTranslatorV2(options) {
  // Welp, this is awkward. Originally the rename was *just* a rename, but then (after the SDK was updated,
  // but before the backend was updated), it was decided that the billing should be simplified at the same time.
  // That's a solid improvement, but it means that the SDK now needs to support both services independently,
  // and correcting the default URL here will break older code, so it must be reserved for a major release.
  // todo: consider checking for options.url === LanguageTranslationV2.URL and also throw this warning then.
  // (This probably does't matter since the api didn't change)
  if (!options.url) {
    const err = new Error(
      'LanguageTranslatorV2 currently defaults to the url for LanguageTranslationV2, ' +
        'but this will change in the next major release of the watson-developer-cloud Node.js SDK. ' +
        'Please either specify the url https://gateway.watsonplatform.net/language-translator/api or else use ' +
        'LanguageTranslationV2. ' +
        'See http://www.ibm.com/watson/developercloud/doc/language-translator/migrating.shtml for more details.'
    );
    // eslint-disable-next-line no-console
    console.warn(err);
  }

  BaseService.call(this, options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.LanguageTranslatorV2.super_"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.LanguageTranslatorV2.</span>super_ (user_options)](#apidoc.element.watson-developer-cloud.LanguageTranslatorV2.super_)
- description and source-code
```javascript
function BaseService(user_options) {
  if (!(this instanceof BaseService)) {
    // it might be better to just create a new instance and return that.. but that can't be done here, it has to be done in each
 individual service. So this is still a good failsafe even in that case.
    throw new Error('"new" keyword required to create Watson service instances');
  }
  let options = extend({}, user_options);

  options = this.initCredentials(options);

  if (options.url) {
    options.url = helper.stripTrailingSlash(options.url);
  }

  this._options = extend({ qs: {}, url: this.constructor.URL }, this.serviceDefaults, options);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.watson-developer-cloud.LanguageTranslatorV2.prototype"></a>[module watson-developer-cloud.LanguageTranslatorV2.prototype](#apidoc.module.watson-developer-cloud.LanguageTranslatorV2.prototype)

#### <a name="apidoc.element.watson-developer-cloud.LanguageTranslatorV2.prototype.createModel"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.LanguageTranslatorV2.prototype.</span>createModel (params, callback)](#apidoc.element.watson-developer-cloud.LanguageTranslatorV2.prototype.createModel)
- description and source-code
```javascript
createModel = function (params, callback) {
  params = params || {};

  const missingParams = helper.getMissingParams(params, ['base_model_id']);
  if (missingParams) {
    callback(missingParams);
    return;
  }

  const inputTypes = ['forced_glossary', 'parallel_corpus', 'monolingual_corpus'];

  for (const type in inputTypes) {
    if (inputTypes.hasOwnProperty(type)) {
      if (params[inputTypes[type]] && !isStream(params[inputTypes[type]])) {
        callback(new Error(inputTypes[type] + ' is not a standard Node.js Stream'));
        return;
      }
    }
  }

  const parameters = {
    options: {
      method: 'POST',
      url: '/v2/models',
      qs: pick(params, ['name', 'base_model_id']),
      formData: pick(params, inputTypes),
      json: true
    },
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.LanguageTranslatorV2.prototype.deleteModel"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.LanguageTranslatorV2.prototype.</span>deleteModel (params, callback)](#apidoc.element.watson-developer-cloud.LanguageTranslatorV2.prototype.deleteModel)
- description and source-code
```javascript
deleteModel = function (params, callback) {
  params = params || {};

  const parameters = {
    options: {
      method: 'DELETE',
      url: '/v2/models/{model_id}',
      path: pick(params, ['model_id']),
      json: true
    },
    requiredParams: ['model_id'],
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.LanguageTranslatorV2.prototype.getIdentifiableLanguages"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.LanguageTranslatorV2.prototype.</span>getIdentifiableLanguages (params, callback)](#apidoc.element.watson-developer-cloud.LanguageTranslatorV2.prototype.getIdentifiableLanguages)
- description and source-code
```javascript
getIdentifiableLanguages = function (params, callback) {
  params = params || {};

  const parameters = {
    options: {
      url: '/v2/identifiable_languages',
      method: 'GET'
    },
    defaultOptions: this._options
  };

  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.LanguageTranslatorV2.prototype.getModel"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.LanguageTranslatorV2.prototype.</span>getModel (params, callback)](#apidoc.element.watson-developer-cloud.LanguageTranslatorV2.prototype.getModel)
- description and source-code
```javascript
getModel = function (params, callback) {
  params = params || {};

  const parameters = {
    options: {
      method: 'GET',
      url: '/v2/models/{model_id}',
      path: pick(params, ['model_id']),
      json: true
    },
    requiredParams: ['model_id'],
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.LanguageTranslatorV2.prototype.getModels"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.LanguageTranslatorV2.prototype.</span>getModels (params, callback)](#apidoc.element.watson-developer-cloud.LanguageTranslatorV2.prototype.getModels)
- description and source-code
```javascript
getModels = function (params, callback) {
  params = params || {};

  const parameters = {
    options: {
      method: 'GET',
      url: '/v2/models',
      qs: pick(params, ['default', 'source', 'target']),
      json: true
    },
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.LanguageTranslatorV2.prototype.identify"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.LanguageTranslatorV2.prototype.</span>identify (params, callback)](#apidoc.element.watson-developer-cloud.LanguageTranslatorV2.prototype.identify)
- description and source-code
```javascript
identify = function (params, callback) {
  if (!params || !params.text) {
    callback(new Error('Missing required parameters: text'));
    return;
  }

  const parameters = {
    options: {
      url: '/v2/identify',
      method: 'POST',
      body: params.text
    },
    defaultOptions: extend(true, {}, this._options, {
      headers: {
        accept: 'application/json',
        'content-type': 'text/plain'
      }
    })
  };

  return requestFactory(parameters, callback);
}
```
- example usage
```shell
...
  function (err, translation) {
    if (err)
      console.log('error:', err);
    else
      console.log(JSON.stringify(translation, null, 2));
});

language_translator.identify({
  text: 'The language translator service takes text input and identifies the language used.' },
  function (err, language) {
    if (err)
      console.log('error:', err);
    else
      console.log(JSON.stringify(language, null, 2));
});
...
```

#### <a name="apidoc.element.watson-developer-cloud.LanguageTranslatorV2.prototype.translate"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.LanguageTranslatorV2.prototype.</span>translate (params, callback)](#apidoc.element.watson-developer-cloud.LanguageTranslatorV2.prototype.translate)
- description and source-code
```javascript
translate = function (params, callback) {
  params = params || {};

  if (!(params.model_id || params.source && params.target)) {
    callback(new Error('Missing required parameters: model_id or source and target'));
    return;
  }
  const parameters = {
    options: {
      url: '/v2/translate',
      method: 'POST',
      json: true,
      body: pick(params, ['source', 'target', 'text', 'model_id'])
    },
    requiredParams: ['text'],
    defaultOptions: this._options
  };

  return requestFactory(parameters, callback);
}
```
- example usage
```shell
...

var language_translator = new LanguageTranslatorV2({
  username: '<username>',
  password: '<password>',
  url: 'https://gateway.watsonplatform.net/language-translator/api/'
});

language_translator.translate({
  text: 'A sentence must have a verb', source : 'en', target: 'es' },
  function (err, translation) {
    if (err)
      console.log('error:', err);
    else
      console.log(JSON.stringify(translation, null, 2));
});
...
```



# <a name="apidoc.module.watson-developer-cloud.NaturalLanguageClassifierV1"></a>[module watson-developer-cloud.NaturalLanguageClassifierV1](#apidoc.module.watson-developer-cloud.NaturalLanguageClassifierV1)

#### <a name="apidoc.element.watson-developer-cloud.NaturalLanguageClassifierV1.NaturalLanguageClassifierV1"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.</span>NaturalLanguageClassifierV1 (options)](#apidoc.element.watson-developer-cloud.NaturalLanguageClassifierV1.NaturalLanguageClassifierV1)
- description and source-code
```javascript
function NaturalLanguageClassifierV1(options) {
  BaseService.call(this, options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.NaturalLanguageClassifierV1.super_"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.NaturalLanguageClassifierV1.</span>super_ (user_options)](#apidoc.element.watson-developer-cloud.NaturalLanguageClassifierV1.super_)
- description and source-code
```javascript
function BaseService(user_options) {
  if (!(this instanceof BaseService)) {
    // it might be better to just create a new instance and return that.. but that can't be done here, it has to be done in each
 individual service. So this is still a good failsafe even in that case.
    throw new Error('"new" keyword required to create Watson service instances');
  }
  let options = extend({}, user_options);

  options = this.initCredentials(options);

  if (options.url) {
    options.url = helper.stripTrailingSlash(options.url);
  }

  this._options = extend({ qs: {}, url: this.constructor.URL }, this.serviceDefaults, options);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.watson-developer-cloud.NaturalLanguageClassifierV1.prototype"></a>[module watson-developer-cloud.NaturalLanguageClassifierV1.prototype](#apidoc.module.watson-developer-cloud.NaturalLanguageClassifierV1.prototype)

#### <a name="apidoc.element.watson-developer-cloud.NaturalLanguageClassifierV1.prototype.classify"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.NaturalLanguageClassifierV1.prototype.</span>classify (params, callback)](#apidoc.element.watson-developer-cloud.NaturalLanguageClassifierV1.prototype.classify)
- description and source-code
```javascript
classify = function (params, callback) {
  params = params || {};

  // #84: use classifier_id not classifier.
  if (!params.classifier_id) {
    params.classifier_id = params.classifier;
  }

  const parameters = {
    options: {
      url: '/v1/classifiers/{classifier_id}/classify',
      method: 'POST',
      json: true,
      path: pick(params, ['classifier_id']),
      body: pick(params, ['text'])
    },
    requiredParams: ['classifier_id', 'text'],
    defaultOptions: this._options
  };

  return requestFactory(parameters, callback);
}
```
- example usage
```shell
...
var NaturalLanguageClassifierV1 = require('watson-developer-cloud/natural-language-classifier/v1');

var natural_language_classifier = new NaturalLanguageClassifierV1({
username: '<username>',
password: '<password>'
});

natural_language_classifier.classify({
text: 'Is it sunny?',
classifier_id: '<classifier-id>' },
function(err, response) {
  if (err)
    console.log('error:', err);
  else
    console.log(JSON.stringify(response, null, 2));
...
```

#### <a name="apidoc.element.watson-developer-cloud.NaturalLanguageClassifierV1.prototype.create"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.NaturalLanguageClassifierV1.prototype.</span>create (params, callback)](#apidoc.element.watson-developer-cloud.NaturalLanguageClassifierV1.prototype.create)
- description and source-code
```javascript
create = function (params, callback) {
  params = params || {};

  if (!params || !params.training_data) {
    callback(new Error('Missing required parameters: training_data'));
    return;
  }
  if (!(Array.isArray(params.training_data) || typeof params.training_data === 'string' || isStream(params.training_data))) {
    callback(new Error('training_data needs to be a String, Array or Stream'));
    return;
  }

  const self = this;

  toCSV(params.training_data, function(err, csv) {
    if (err) {
      callback(err);
      return;
    }

    const parameters = {
      options: {
        url: '/v1/classifiers',
        method: 'POST',
        json: true,
        formData: {
          training_data: csv,
          training_metadata: JSON.stringify(omit(params, ['training_data']))
        },
        // hack to check required parameters.
        // We don't actually need path parameters
        path: pick(params, ['language'])
      },
      requiredParams: ['language'],
      defaultOptions: self._options
    };
    return requestFactory(parameters, callback);
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.NaturalLanguageClassifierV1.prototype.list"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.NaturalLanguageClassifierV1.prototype.</span>list (params, callback)](#apidoc.element.watson-developer-cloud.NaturalLanguageClassifierV1.prototype.list)
- description and source-code
```javascript
list = function (params, callback) {
  const parameters = {
    options: {
      url: '/v1/classifiers',
      method: 'GET',
      json: true
    },
    defaultOptions: this._options
  };

  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.NaturalLanguageClassifierV1.prototype.remove"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.NaturalLanguageClassifierV1.prototype.</span>remove (params, callback)](#apidoc.element.watson-developer-cloud.NaturalLanguageClassifierV1.prototype.remove)
- description and source-code
```javascript
remove = function (params, callback) {
  params = params || {};

  // #84: use classifier_id not classifier.
  if (!params.classifier_id) {
    params.classifier_id = params.classifier;
  }

  const parameters = {
    options: {
      url: '/v1/classifiers/{classifier_id}',
      method: 'DELETE',
      path: params,
      json: true
    },
    requiredParams: ['classifier_id'],
    defaultOptions: this._options
  };

  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.NaturalLanguageClassifierV1.prototype.status"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.NaturalLanguageClassifierV1.prototype.</span>status (params, callback)](#apidoc.element.watson-developer-cloud.NaturalLanguageClassifierV1.prototype.status)
- description and source-code
```javascript
status = function (params, callback) {
  params = params || {};

  // #84: use classifier_id not classifier.
  if (!params.classifier_id) {
    params.classifier_id = params.classifier;
  }

  const parameters = {
    options: {
      url: '/v1/classifiers/{classifier_id}',
      method: 'GET',
      json: true,
      path: params
    },
    requiredParams: ['classifier_id'],
    defaultOptions: this._options
  };

  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.watson-developer-cloud.NaturalLanguageUnderstandingV1"></a>[module watson-developer-cloud.NaturalLanguageUnderstandingV1](#apidoc.module.watson-developer-cloud.NaturalLanguageUnderstandingV1)

#### <a name="apidoc.element.watson-developer-cloud.NaturalLanguageUnderstandingV1.NaturalLanguageUnderstandingV1"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.</span>NaturalLanguageUnderstandingV1 (options)](#apidoc.element.watson-developer-cloud.NaturalLanguageUnderstandingV1.NaturalLanguageUnderstandingV1)
- description and source-code
```javascript
function NaturalLanguageUnderstandingV1(options) {
  BaseService.call(this, options);
  if (typeof this._options.version_date === 'undefined') {
    throw new Error('Argument error: version_date was not specified, use NaturalLanguageUnderstandingV1.VERSION_DATE_2017_02_27');
  }
  this._options.qs.version = this._options.version_date;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.NaturalLanguageUnderstandingV1.super_"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.NaturalLanguageUnderstandingV1.</span>super_ (user_options)](#apidoc.element.watson-developer-cloud.NaturalLanguageUnderstandingV1.super_)
- description and source-code
```javascript
function BaseService(user_options) {
  if (!(this instanceof BaseService)) {
    // it might be better to just create a new instance and return that.. but that can't be done here, it has to be done in each
 individual service. So this is still a good failsafe even in that case.
    throw new Error('"new" keyword required to create Watson service instances');
  }
  let options = extend({}, user_options);

  options = this.initCredentials(options);

  if (options.url) {
    options.url = helper.stripTrailingSlash(options.url);
  }

  this._options = extend({ qs: {}, url: this.constructor.URL }, this.serviceDefaults, options);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.watson-developer-cloud.NaturalLanguageUnderstandingV1.prototype"></a>[module watson-developer-cloud.NaturalLanguageUnderstandingV1.prototype](#apidoc.module.watson-developer-cloud.NaturalLanguageUnderstandingV1.prototype)

#### <a name="apidoc.element.watson-developer-cloud.NaturalLanguageUnderstandingV1.prototype.analyze"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.NaturalLanguageUnderstandingV1.prototype.</span>analyze (params, callback)](#apidoc.element.watson-developer-cloud.NaturalLanguageUnderstandingV1.prototype.analyze)
- description and source-code
```javascript
analyze = function (params, callback) {
  const parameters = {
    options: {
      url: '/v1/analyze',
      method: 'POST',
      json: true,
      body: params
    },
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
...

var nlu = new NaturalLanguageUnderstandingV1({
  username: '<username>',
  password: '<password>',
  version_date: NaturalLanguageUnderstandingV1.VERSION_DATE_2017_02_27
});

nlu.analyze({
  'html': file_data, // Buffer or String
  'features': {
    'concepts': {},
    'keywords': {},
  }
}, function(err, response) {
if (err)
...
```

#### <a name="apidoc.element.watson-developer-cloud.NaturalLanguageUnderstandingV1.prototype.deleteModel"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.NaturalLanguageUnderstandingV1.prototype.</span>deleteModel (params, callback)](#apidoc.element.watson-developer-cloud.NaturalLanguageUnderstandingV1.prototype.deleteModel)
- description and source-code
```javascript
deleteModel = function (params, callback) {
  const parameters = {
    options: {
      method: 'DELETE',
      url: '/v1/models/{model_id}',
      path: params,
      json: true
    },
    requiredParams: ['model_id'],
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.NaturalLanguageUnderstandingV1.prototype.getCredentialsFromBluemix"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.NaturalLanguageUnderstandingV1.prototype.</span>getCredentialsFromBluemix (name)](#apidoc.element.watson-developer-cloud.NaturalLanguageUnderstandingV1.prototype.getCredentialsFromBluemix)
- description and source-code
```javascript
getCredentialsFromBluemix = function (name) {
  return extend(
    {},
    BaseService.prototype.getCredentialsFromBluemix.call(this, name),
    BaseService.prototype.getCredentialsFromBluemix.call(this, name.replace(/_/g, '-'))
  );
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.NaturalLanguageUnderstandingV1.prototype.listModels"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.NaturalLanguageUnderstandingV1.prototype.</span>listModels (params, callback)](#apidoc.element.watson-developer-cloud.NaturalLanguageUnderstandingV1.prototype.listModels)
- description and source-code
```javascript
listModels = function (params, callback) {
  const parameters = {
    options: {
      url: '/v1/models',
      method: 'GET',
      json: true
    },
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.watson-developer-cloud.PersonalityInsightsV2"></a>[module watson-developer-cloud.PersonalityInsightsV2](#apidoc.module.watson-developer-cloud.PersonalityInsightsV2)

#### <a name="apidoc.element.watson-developer-cloud.PersonalityInsightsV2.PersonalityInsightsV2"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.</span>PersonalityInsightsV2 (options)](#apidoc.element.watson-developer-cloud.PersonalityInsightsV2.PersonalityInsightsV2)
- description and source-code
```javascript
function PersonalityInsightsV2(options) {
  BaseService.call(this, options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.PersonalityInsightsV2.super_"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.PersonalityInsightsV2.</span>super_ (user_options)](#apidoc.element.watson-developer-cloud.PersonalityInsightsV2.super_)
- description and source-code
```javascript
function BaseService(user_options) {
  if (!(this instanceof BaseService)) {
    // it might be better to just create a new instance and return that.. but that can't be done here, it has to be done in each
 individual service. So this is still a good failsafe even in that case.
    throw new Error('"new" keyword required to create Watson service instances');
  }
  let options = extend({}, user_options);

  options = this.initCredentials(options);

  if (options.url) {
    options.url = helper.stripTrailingSlash(options.url);
  }

  this._options = extend({ qs: {}, url: this.constructor.URL }, this.serviceDefaults, options);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.watson-developer-cloud.PersonalityInsightsV2.prototype"></a>[module watson-developer-cloud.PersonalityInsightsV2.prototype](#apidoc.module.watson-developer-cloud.PersonalityInsightsV2.prototype)

#### <a name="apidoc.element.watson-developer-cloud.PersonalityInsightsV2.prototype.profile"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.PersonalityInsightsV2.prototype.</span>profile ( params, callback // eslint-disable-line complexity )](#apidoc.element.watson-developer-cloud.PersonalityInsightsV2.prototype.profile)
- description and source-code
```javascript
profile = function ( params, callback // eslint-disable-line complexity ) {
  params = params || {};

  // support for the new snake_case
  if (params.content_items) {
    params.contentItems = params.content_items;
  }

  if (!params.text && !params.contentItems) {
    callback(new Error('Missing required parameters: text or content_items'));
    return;
  }

  // Content-Type
  let content_type = null;
  if (params.text) {
    content_type = helper.isHTML(params.text) ? 'text/html' : 'text/plain';
  } else {
    content_type = 'application/json';
  }

  const headers = {
    'Content-type': content_type,
    'Accept-language': params.accept_language || params.acceptLanguage || 'en'
  };

  // service bug: language in header overrides language in each JSON content item, so we can't set it on those requests
  // (also, content-language doesn't really make sense on JSON)
  if (params.language || params.text) {
    headers['Content-language'] = params.language || 'en';
  }

  const parameters = {
    options: {
      method: 'POST',
      url: '/v2/profile',
      body: params.text || pick(params, ['contentItems']),
      json: true,
      qs: pick(params, ['include_raw']),
      headers: headers
    },
    defaultOptions: this._options
  };

  if (params.csv) {
    parameters.options.headers.Accept = 'text/csv';
    if (params.csv_headers) {
      parameters.options.qs.headers = 'true';
    }
  }

  return requestFactory(parameters, callback);
}
```
- example usage
```shell
...

var personality_insights = new PersonalityInsightsV3({
username: '<username>',
password: '<password>',
version_date: '2016-10-19'
});

personality_insights.profile({
text: 'Enter more than 100 unique words here...',
consumption_preferences: true
},
function (err, response) {
  if (err)
    console.log('error:', err);
  else
...
```



# <a name="apidoc.module.watson-developer-cloud.PersonalityInsightsV3"></a>[module watson-developer-cloud.PersonalityInsightsV3](#apidoc.module.watson-developer-cloud.PersonalityInsightsV3)

#### <a name="apidoc.element.watson-developer-cloud.PersonalityInsightsV3.PersonalityInsightsV3"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.</span>PersonalityInsightsV3 (options)](#apidoc.element.watson-developer-cloud.PersonalityInsightsV3.PersonalityInsightsV3)
- description and source-code
```javascript
function PersonalityInsightsV3(options) {
  BaseService.call(this, options);

  // Check if 'version_date' was provided
  if (typeof this._options.version_date === 'undefined') {
    throw new Error('Argument error: version_date was not specified, use 2016-10-19');
  }
  this._options.qs.version = options.version_date;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.PersonalityInsightsV3.super_"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.PersonalityInsightsV3.</span>super_ (user_options)](#apidoc.element.watson-developer-cloud.PersonalityInsightsV3.super_)
- description and source-code
```javascript
function BaseService(user_options) {
  if (!(this instanceof BaseService)) {
    // it might be better to just create a new instance and return that.. but that can't be done here, it has to be done in each
 individual service. So this is still a good failsafe even in that case.
    throw new Error('"new" keyword required to create Watson service instances');
  }
  let options = extend({}, user_options);

  options = this.initCredentials(options);

  if (options.url) {
    options.url = helper.stripTrailingSlash(options.url);
  }

  this._options = extend({ qs: {}, url: this.constructor.URL }, this.serviceDefaults, options);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.watson-developer-cloud.PersonalityInsightsV3.prototype"></a>[module watson-developer-cloud.PersonalityInsightsV3.prototype](#apidoc.module.watson-developer-cloud.PersonalityInsightsV3.prototype)

#### <a name="apidoc.element.watson-developer-cloud.PersonalityInsightsV3.prototype.profile"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.PersonalityInsightsV3.prototype.</span>profile ( _params, callback // eslint-disable-line complexity )](#apidoc.element.watson-developer-cloud.PersonalityInsightsV3.prototype.profile)
- description and source-code
```javascript
profile = function ( _params, callback // eslint-disable-line complexity ) {
  const params = extend({}, _params);

  if (params.content_items) {
    params.contentItems = params.content_items;
  }

  if (!params.text && !params.contentItems) {
    callback(new Error('Missing required parameters: text or content_items'));
    return;
  }

  // Content-Type
  let content_type = null;
  if (params.text) {
    content_type = helper.isHTML(params.text) ? 'text/html' : 'text/plain';
  } else {
    content_type = 'application/json';
  }

  const parameters = {
    options: {
      method: 'POST',
      url: '/v3/profile',
      body: params.text || pick(params, ['contentItems']),
      json: true,
      qs: pick(params, ['csv_headers', 'raw_scores', 'consumption_preferences']),
      headers: extend({ 'content-type': content_type, 'accept-language': 'en' }, params.headers)
    },
    defaultOptions: this._options
  };

  return requestFactory(parameters, callback);
}
```
- example usage
```shell
...

var personality_insights = new PersonalityInsightsV3({
username: '<username>',
password: '<password>',
version_date: '2016-10-19'
});

personality_insights.profile({
text: 'Enter more than 100 unique words here...',
consumption_preferences: true
},
function (err, response) {
  if (err)
    console.log('error:', err);
  else
...
```



# <a name="apidoc.module.watson-developer-cloud.RetrieveAndRankV1"></a>[module watson-developer-cloud.RetrieveAndRankV1](#apidoc.module.watson-developer-cloud.RetrieveAndRankV1)

#### <a name="apidoc.element.watson-developer-cloud.RetrieveAndRankV1.RetrieveAndRankV1"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.</span>RetrieveAndRankV1 (options)](#apidoc.element.watson-developer-cloud.RetrieveAndRankV1.RetrieveAndRankV1)
- description and source-code
```javascript
function RetrieveAndRankV1(options) {
  BaseService.call(this, options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.RetrieveAndRankV1.super_"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.RetrieveAndRankV1.</span>super_ (user_options)](#apidoc.element.watson-developer-cloud.RetrieveAndRankV1.super_)
- description and source-code
```javascript
function BaseService(user_options) {
  if (!(this instanceof BaseService)) {
    // it might be better to just create a new instance and return that.. but that can't be done here, it has to be done in each
 individual service. So this is still a good failsafe even in that case.
    throw new Error('"new" keyword required to create Watson service instances');
  }
  let options = extend({}, user_options);

  options = this.initCredentials(options);

  if (options.url) {
    options.url = helper.stripTrailingSlash(options.url);
  }

  this._options = extend({ qs: {}, url: this.constructor.URL }, this.serviceDefaults, options);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.watson-developer-cloud.RetrieveAndRankV1.prototype"></a>[module watson-developer-cloud.RetrieveAndRankV1.prototype](#apidoc.module.watson-developer-cloud.RetrieveAndRankV1.prototype)

#### <a name="apidoc.element.watson-developer-cloud.RetrieveAndRankV1.prototype.createCluster"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.RetrieveAndRankV1.prototype.</span>createCluster (params, callback)](#apidoc.element.watson-developer-cloud.RetrieveAndRankV1.prototype.createCluster)
- description and source-code
```javascript
createCluster = function (params, callback) {
  params = params || {};

  const parameters = {
    options: {
      url: '/v1/solr_clusters',
      method: 'POST',
      json: true,
      body: params
    },
    defaultOptions: this._options
  };

  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.RetrieveAndRankV1.prototype.createCollection"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.RetrieveAndRankV1.prototype.</span>createCollection (params, callback)](#apidoc.element.watson-developer-cloud.RetrieveAndRankV1.prototype.createCollection)
- description and source-code
```javascript
createCollection = function (params, callback) {
  params = params || {};

  const missingParams = helper.getMissingParams(params, ['cluster_id', 'collection_name', 'config_name']);
  if (missingParams) {
    callback(missingParams);
    return;
  }

  const queryParams = {
    'collection.configName': params.config_name,
    name: params.collection_name,
    wt: params.wt || 'json',
    action: 'CREATE'
  };

  const parameters = {
    options: {
      url: '/v1/solr_clusters/{cluster_id}/solr/admin/collections',
      method: 'POST',
      qs: queryParams,
      path: pick(params, ['cluster_id']),
      json: true
    },
    defaultOptions: this._options
  };

  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.RetrieveAndRankV1.prototype.createRanker"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.RetrieveAndRankV1.prototype.</span>createRanker (params, callback)](#apidoc.element.watson-developer-cloud.RetrieveAndRankV1.prototype.createRanker)
- description and source-code
```javascript
createRanker = function (params, callback) {
  params = params || {};

  if (!params || !params.training_data) {
    callback(new Error('Missing required parameters: training_data'));
    return;
  }
  if (typeof params.training_data !== 'string' && !isStream(params.training_data)) {
    callback(new Error('training_data needs to be a String or Stream'));
    return;
  }

  const parameters = {
    options: {
      url: '/v1/rankers',
      method: 'POST',
      json: true,
      formData: {
        training_data: params.training_data,
        training_metadata: params.training_metadata || JSON.stringify(omit(params, ['training_data']))
      }
    },
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.RetrieveAndRankV1.prototype.createSolrClient"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.RetrieveAndRankV1.prototype.</span>createSolrClient (params)](#apidoc.element.watson-developer-cloud.RetrieveAndRankV1.prototype.createSolrClient)
- description and source-code
```javascript
createSolrClient = function (params) {
  params = params || {};

  const missingParams = helper.getMissingParams(params, ['cluster_id', 'collection_name']);
  if (missingParams) {
    throw missingParams;
  }

  const serviceUrl = url.parse(this._options.url);
  const apiPath = serviceUrl.path === '/' ? '' : serviceUrl.path || '';

  const solrClient = solr.createClient({
    host: serviceUrl.hostname,
    path: apiPath + '/v1/solr_clusters/' + params.cluster_id + '/solr',
    port: serviceUrl.port || '443',
    secure: true,
    core: params.collection_name
  });

  if (this._options.username && this._options.password) {
    solrClient.basicAuth(this._options.username, this._options.password);
  }
  return solrClient;
}
```
- example usage
```shell
...
var RetrieveAndRankV1 = require('watson-developer-cloud/retrieve-and-rank/v1');

var retrieve = new RetrieveAndRankV1({
  username: '<username>',
  password: '<password>',
});

var solrClient = retrieve.createSolrClient({
  cluster_id: 'INSERT YOUR CLUSTER ID HERE',
  collection_name: 'example_collection'
});

// add a document
var doc = { id : 1234, title_t : 'Hello', text_field_s: 'some text' };
solrClient.add(doc, function(err) {
...
```

#### <a name="apidoc.element.watson-developer-cloud.RetrieveAndRankV1.prototype.deleteCluster"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.RetrieveAndRankV1.prototype.</span>deleteCluster (params, callback)](#apidoc.element.watson-developer-cloud.RetrieveAndRankV1.prototype.deleteCluster)
- description and source-code
```javascript
deleteCluster = function (params, callback) {
  params = params || {};

  const parameters = {
    options: {
      url: '/v1/solr_clusters/{cluster_id}',
      method: 'DELETE',
      path: params,
      json: true
    },
    requiredParams: ['cluster_id'],
    defaultOptions: this._options
  };

  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.RetrieveAndRankV1.prototype.deleteCollection"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.RetrieveAndRankV1.prototype.</span>deleteCollection (params, callback)](#apidoc.element.watson-developer-cloud.RetrieveAndRankV1.prototype.deleteCollection)
- description and source-code
```javascript
deleteCollection = function (params, callback) {
  params = params || {};

  const missingParams = helper.getMissingParams(params, ['cluster_id', 'collection_name']);
  if (missingParams) {
    callback(missingParams);
    return;
  }

  const queryParams = {
    name: params.collection_name,
    wt: params.wt || 'json',
    action: 'DELETE'
  };

  const parameters = {
    options: {
      url: '/v1/solr_clusters/{cluster_id}/solr/admin/collections',
      method: 'POST',
      qs: queryParams,
      path: pick(params, ['cluster_id']),
      json: true
    },
    defaultOptions: this._options
  };

  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.RetrieveAndRankV1.prototype.deleteConfig"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.RetrieveAndRankV1.prototype.</span>deleteConfig (params, callback)](#apidoc.element.watson-developer-cloud.RetrieveAndRankV1.prototype.deleteConfig)
- description and source-code
```javascript
deleteConfig = function (params, callback) {
  params = params || {};

  const parameters = {
    options: {
      url: '/v1/solr_clusters/{cluster_id}/config/{config_name}',
      method: 'DELETE',
      path: params,
      json: true
    },
    requiredParams: ['cluster_id', 'config_name'],
    defaultOptions: this._options
  };

  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.RetrieveAndRankV1.prototype.deleteRanker"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.RetrieveAndRankV1.prototype.</span>deleteRanker (params, callback)](#apidoc.element.watson-developer-cloud.RetrieveAndRankV1.prototype.deleteRanker)
- description and source-code
```javascript
deleteRanker = function (params, callback) {
  params = params || {};

  const parameters = {
    options: {
      url: '/v1/rankers/{ranker_id}',
      method: 'DELETE',
      path: params,
      json: true
    },
    requiredParams: ['ranker_id'],
    defaultOptions: this._options
  };

  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.RetrieveAndRankV1.prototype.getClusterStats"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.RetrieveAndRankV1.prototype.</span>getClusterStats (params, callback)](#apidoc.element.watson-developer-cloud.RetrieveAndRankV1.prototype.getClusterStats)
- description and source-code
```javascript
getClusterStats = function (params, callback) {
  params = params || {};

  const parameters = {
    options: {
      url: '/v1/solr_clusters/{cluster_id}/stats',
      method: 'GET',
      path: params,
      json: true
    },
    requiredParams: ['cluster_id'],
    defaultOptions: this._options
  };

  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.RetrieveAndRankV1.prototype.getConfig"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.RetrieveAndRankV1.prototype.</span>getConfig (params, callback)](#apidoc.element.watson-developer-cloud.RetrieveAndRankV1.prototype.getConfig)
- description and source-code
```javascript
getConfig = function (params, callback) {
  params = params || {};

  const parameters = {
    options: {
      url: '/v1/solr_clusters/{cluster_id}/config/{config_name}',
      method: 'GET',
      path: params,
      json: true,
      headers: {
        accept: 'application/zip'
      }
    },
    requiredParams: ['cluster_id', 'config_name'],
    defaultOptions: this._options
  };

  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.RetrieveAndRankV1.prototype.getResizeStatus"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.RetrieveAndRankV1.prototype.</span>getResizeStatus (params, callback)](#apidoc.element.watson-developer-cloud.RetrieveAndRankV1.prototype.getResizeStatus)
- description and source-code
```javascript
getResizeStatus = function (params, callback) {
  params = params || {};

  const parameters = {
    options: {
      url: '/v1/solr_clusters/{cluster_id}/cluster_size',
      method: 'GET',
      path: params,
      json: true
    },
    requiredParams: ['cluster_id'],
    defaultOptions: this._options
  };

  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.RetrieveAndRankV1.prototype.listClusters"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.RetrieveAndRankV1.prototype.</span>listClusters (params, callback)](#apidoc.element.watson-developer-cloud.RetrieveAndRankV1.prototype.listClusters)
- description and source-code
```javascript
listClusters = function (params, callback) {
  params = params || {};

  const parameters = {
    options: {
      url: '/v1/solr_clusters',
      method: 'GET',
      json: true
    },
    defaultOptions: this._options
  };

  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.RetrieveAndRankV1.prototype.listCollections"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.RetrieveAndRankV1.prototype.</span>listCollections (params, callback)](#apidoc.element.watson-developer-cloud.RetrieveAndRankV1.prototype.listCollections)
- description and source-code
```javascript
listCollections = function (params, callback) {
  params = params || {};
  const parameters = {
    options: {
      url: '/v1/solr_clusters/{cluster_id}/solr/admin/collections',
      method: 'GET',
      qs: {
        action: 'LIST',
        wt: params.wt || 'json'
      },
      path: params,
      json: true
    },
    requiredParams: ['cluster_id'],
    defaultOptions: this._options
  };

  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.RetrieveAndRankV1.prototype.listConfigs"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.RetrieveAndRankV1.prototype.</span>listConfigs (params, callback)](#apidoc.element.watson-developer-cloud.RetrieveAndRankV1.prototype.listConfigs)
- description and source-code
```javascript
listConfigs = function (params, callback) {
  params = params || {};

  const parameters = {
    options: {
      url: '/v1/solr_clusters/{cluster_id}/config',
      method: 'GET',
      path: params,
      json: true
    },
    requiredParams: ['cluster_id'],
    defaultOptions: this._options
  };

  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.RetrieveAndRankV1.prototype.listRankers"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.RetrieveAndRankV1.prototype.</span>listRankers (params, callback)](#apidoc.element.watson-developer-cloud.RetrieveAndRankV1.prototype.listRankers)
- description and source-code
```javascript
listRankers = function (params, callback) {
  const parameters = {
    options: {
      url: '/v1/rankers',
      method: 'GET',
      json: true
    },
    defaultOptions: this._options
  };

  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.RetrieveAndRankV1.prototype.pollCluster"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.RetrieveAndRankV1.prototype.</span>pollCluster (params, callback)](#apidoc.element.watson-developer-cloud.RetrieveAndRankV1.prototype.pollCluster)
- description and source-code
```javascript
pollCluster = function (params, callback) {
  params = params || {};

  const parameters = {
    options: {
      url: '/v1/solr_clusters/{cluster_id}',
      method: 'GET',
      path: params,
      json: true
    },
    requiredParams: ['cluster_id'],
    defaultOptions: this._options
  };

  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.RetrieveAndRankV1.prototype.rank"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.RetrieveAndRankV1.prototype.</span>rank (params, callback)](#apidoc.element.watson-developer-cloud.RetrieveAndRankV1.prototype.rank)
- description and source-code
```javascript
rank = function (params, callback) {
  params = params || {};

  if (!params || !params.answer_data) {
    callback(new Error('Missing required parameters: answer_data'));
    return;
  }
  if (typeof params.answer_data !== 'string' && !isStream(params.answer_data)) {
    callback(new Error('answer_data needs to be a String or Stream'));
    return;
  }

  const topLevelParams = ['answer_data', 'answers'];
  const formData = pick(params, topLevelParams);
  formData.answer_metadata = JSON.stringify(omit(params, topLevelParams));

  const parameters = {
    options: {
      url: '/v1/rankers/{ranker_id}/rank',
      method: 'POST',
      json: true,
      formData: formData,
      path: pick(params, ['ranker_id'])
    },
    requiredParams: ['ranker_id'],
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.RetrieveAndRankV1.prototype.rankerStatus"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.RetrieveAndRankV1.prototype.</span>rankerStatus (params, callback)](#apidoc.element.watson-developer-cloud.RetrieveAndRankV1.prototype.rankerStatus)
- description and source-code
```javascript
rankerStatus = function (params, callback) {
  params = params || {};

  const parameters = {
    options: {
      url: '/v1/rankers/{ranker_id}',
      method: 'GET',
      json: true,
      path: params
    },
    requiredParams: ['ranker_id'],
    defaultOptions: this._options
  };

  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.RetrieveAndRankV1.prototype.resizeCluster"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.RetrieveAndRankV1.prototype.</span>resizeCluster (params, callback)](#apidoc.element.watson-developer-cloud.RetrieveAndRankV1.prototype.resizeCluster)
- description and source-code
```javascript
resizeCluster = function (params, callback) {
  params = params || {};

  const parameters = {
    options: {
      url: '/v1/solr_clusters/{cluster_id}/cluster_size',
      method: 'PUT',
      body: { cluster_size: params.cluster_size },
      path: params,
      json: true
    },
    requiredParams: ['cluster_id', 'cluster_size'],
    defaultOptions: this._options
  };

  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.RetrieveAndRankV1.prototype.uploadConfig"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.RetrieveAndRankV1.prototype.</span>uploadConfig (params, callback)](#apidoc.element.watson-developer-cloud.RetrieveAndRankV1.prototype.uploadConfig)
- description and source-code
```javascript
uploadConfig = function (params, callback) {
  params = params || {};

  if (!params || !params.config_zip_path) {
    callback(new Error('Missing required parameters: config_zip_path'));
    return;
  }
  let configFile = null;
  if (typeof params.config_zip_path === 'string') {
    configFile = fs.createReadStream(params.config_zip_path);
  } else if (isStream(params.config_zip_path)) {
    configFile = params.config_zip_path;
  } else {
    callback(new Error('config_zip_path needs to be a String or Stream'));
    return;
  }

  const parameters = {
    options: {
      url: '/v1/solr_clusters/{cluster_id}/config/{config_name}',
      method: 'POST',
      path: params
    },
    requiredParams: ['cluster_id', 'config_name'],
    defaultOptions: this._options
  };

  return configFile
    .on('response', function(response) {
      // Replace content-type
      response.headers['content-type'] = 'application/zip';
    })
    .pipe(requestFactory(parameters, callback));
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.watson-developer-cloud.SpeechToTextV1"></a>[module watson-developer-cloud.SpeechToTextV1](#apidoc.module.watson-developer-cloud.SpeechToTextV1)

#### <a name="apidoc.element.watson-developer-cloud.SpeechToTextV1.SpeechToTextV1"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.</span>SpeechToTextV1 (options)](#apidoc.element.watson-developer-cloud.SpeechToTextV1.SpeechToTextV1)
- description and source-code
```javascript
function SpeechToTextV1(options) {
  BaseService.call(this, options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.SpeechToTextV1.super_"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.SpeechToTextV1.</span>super_ (user_options)](#apidoc.element.watson-developer-cloud.SpeechToTextV1.super_)
- description and source-code
```javascript
function BaseService(user_options) {
  if (!(this instanceof BaseService)) {
    // it might be better to just create a new instance and return that.. but that can't be done here, it has to be done in each
 individual service. So this is still a good failsafe even in that case.
    throw new Error('"new" keyword required to create Watson service instances');
  }
  let options = extend({}, user_options);

  options = this.initCredentials(options);

  if (options.url) {
    options.url = helper.stripTrailingSlash(options.url);
  }

  this._options = extend({ qs: {}, url: this.constructor.URL }, this.serviceDefaults, options);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.watson-developer-cloud.SpeechToTextV1.prototype"></a>[module watson-developer-cloud.SpeechToTextV1.prototype](#apidoc.module.watson-developer-cloud.SpeechToTextV1.prototype)

#### <a name="apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.addCorpus"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.SpeechToTextV1.prototype.</span>addCorpus (params, callback)](#apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.addCorpus)
- description and source-code
```javascript
addCorpus = function (params, callback) {
  const parameters = {
    requiredParams: ['customization_id', 'name', 'corpus'],
    originalParams: params,
    options: {
      method: 'POST', // shouldn't this be a PUT?
      url: '/v1/customizations/{customization_id}/corpora/{name}',
      path: pick(params, ['customization_id', 'name']),
      qs: pick(params, ['allow_overwrite']),
      body: params.corpus
    },
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.addWord"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.SpeechToTextV1.prototype.</span>addWord (params, callback)](#apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.addWord)
- description and source-code
```javascript
addWord = function (params, callback) {
  const parameters = {
    requiredParams: ['customization_id', 'word', 'sounds_like'],
    options: {
      method: 'PUT',
      url: '/v1/customizations/{customization_id}/words/{word}',
      path: pick(params, ['customization_id', 'word']),
      body: pick(params, ['sounds_like', 'display_as']),
      json: true
    },
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.addWords"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.SpeechToTextV1.prototype.</span>addWords (params, callback)](#apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.addWords)
- description and source-code
```javascript
addWords = function (params, callback) {
  const parameters = {
    requiredParams: ['customization_id', 'words'],
    options: {
      method: 'POST',
      url: '/v1/customizations/{customization_id}/words',
      path: pick(params, ['customization_id']),
      body: pick(params, ['words']),
      json: true
    },
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.createCustomization"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.SpeechToTextV1.prototype.</span>createCustomization (params, callback)](#apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.createCustomization)
- description and source-code
```javascript
createCustomization = function (params, callback) {
  const parameters = {
    requiredParams: ['base_model_name', 'name'],
    options: {
      method: 'POST',
      url: '/v1/customizations',
      body: pick(params, ['name', 'base_model_name', 'description']),
      json: true
    },
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.createRecognitionJob"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.SpeechToTextV1.prototype.</span>createRecognitionJob (params, callback)](#apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.createRecognitionJob)
- description and source-code
```javascript
createRecognitionJob = function (params, callback) {
  const missingParams = helper.getMissingParams(params, ['audio', 'content_type']);
  if (missingParams) {
    callback(missingParams);
    return;
  }

  if (!isStream(params.audio)) {
    callback(new Error('audio is not a standard Node.js Stream'));
    return;
  }

  const qs = pick(params, ['callback_url', 'events', 'user_token', 'results_ttl'].concat(PARAMS_ALLOWED));

  // multiple events must be sent as a comma-separated string. Default behavior is multiple &event= params in the querystring
  if (Array.isArray(qs.events)) {
    qs.events = qs.events.join(',');
  }

  const parameters = {
    options: {
      method: 'POST',
      url: '/v1/recognitions',
      headers: {
        'Content-Type': params.content_type
      },
      qs: qs,
      json: true
    },
    defaultOptions: this._options
  };

  return params.audio
    .on('response', function(response) {
      // Replace content-type
      response.headers['content-type'] = params.content_type;
    })
    .pipe(requestFactory(parameters, callback));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.createRecognizeStream"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.SpeechToTextV1.prototype.</span>createRecognizeStream (params)](#apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.createRecognizeStream)
- description and source-code
```javascript
createRecognizeStream = function (params) {
  params = params || {};
  params.url = this._options.url;

  params.headers = extend(
    {
      'user-agent': pkg.name + '-nodejs-' + pkg.version,
      authorization: this._options.headers.Authorization
    },
    params.headers
  );

  return new RecognizeStream(params);
}
```
- example usage
```shell
...
    console.log(err);
  else
    console.log(JSON.stringify(res, null, 2));
});

// or streaming
fs.createReadStream('./resources/speech.wav')
  .pipe(speech_to_text.createRecognizeStream({ content_type: 'audio/l16; rate=44100' }))
  .pipe(fs.createWriteStream('./transcription.txt'));
'''

### Text to Speech
Use the [Text to Speech][text_to_speech] service to synthesize text into a .wav file.

'''js
...
```

#### <a name="apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.createSession"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.SpeechToTextV1.prototype.</span>createSession (params, callback)](#apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.createSession)
- description and source-code
```javascript
createSession = function (params, callback) {
  const parameters = {
    options: {
      method: 'POST',
      url: '/v1/sessions',
      json: true,
      qs: params
    },
    defaultOptions: this._options
  };

<span class="apidocCodeCommentSpan">  /**
   * Add the cookie_session to the response
   * @private
   * @param cb
   * @return {Function}
   */
</span>  function addSessionId(cb) {
    return function(error, body, response) {
      if (error) {
        cb(error, body, response);
        return;
      }
      const cookies = cookie.parse(response.headers['set-cookie'][0]);
      body.cookie_session = cookies.SESSIONID;
      cb(error, body, response);
    };
  }

  return requestFactory(parameters, addSessionId(callback));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.deleteCorpus"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.SpeechToTextV1.prototype.</span>deleteCorpus (params, callback)](#apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.deleteCorpus)
- description and source-code
```javascript
deleteCorpus = function (params, callback) {
  const parameters = {
    requiredParams: ['customization_id', 'name'],
    options: {
      method: 'DELETE',
      url: '/v1/customizations/{customization_id}/corpora/{name}',
      path: pick(params, ['customization_id', 'name']),
      json: true
    },
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.deleteCustomization"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.SpeechToTextV1.prototype.</span>deleteCustomization (params, callback)](#apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.deleteCustomization)
- description and source-code
```javascript
deleteCustomization = function (params, callback) {
  const parameters = {
    requiredParams: ['customization_id'],
    options: {
      method: 'DELETE',
      url: '/v1/customizations/{customization_id}',
      path: pick(params, ['customization_id']),
      json: true
    },
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.deleteRecognitionJob"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.SpeechToTextV1.prototype.</span>deleteRecognitionJob (params, callback)](#apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.deleteRecognitionJob)
- description and source-code
```javascript
deleteRecognitionJob = function (params, callback) {
  const missingParams = helper.getMissingParams(params, ['id']);
  if (missingParams) {
    callback(missingParams);
    return;
  }

  const parameters = {
    options: {
      method: 'DELETE',
      url: '/v1/recognitions/{id}',
      path: pick(params, ['id']),
      json: true
    },
    defaultOptions: this._options
  };

  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.deleteSession"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.SpeechToTextV1.prototype.</span>deleteSession (params, callback)](#apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.deleteSession)
- description and source-code
```javascript
deleteSession = function (params, callback) {
  const parameters = {
    requiredParams: ['session_id'],
    options: {
      method: 'DELETE',
      url: '/v1/sessions/{session_id}',
      json: true,
      path: pick(params, ['session_id'])
    },
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.deleteWord"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.SpeechToTextV1.prototype.</span>deleteWord (params, callback)](#apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.deleteWord)
- description and source-code
```javascript
deleteWord = function (params, callback) {
  const parameters = {
    requiredParams: ['customization_id', 'word'],
    options: {
      method: 'DELETE',
      url: '/v1/customizations/{customization_id}/words/{word}',
      path: pick(params, ['customization_id', 'word']),
      json: true
    },
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.getCorpora"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.SpeechToTextV1.prototype.</span>getCorpora (params, callback)](#apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.getCorpora)
- description and source-code
```javascript
getCorpora = function (params, callback) {
  const parameters = {
    requiredParams: ['customization_id'],
    options: {
      method: 'GET',
      url: '/v1/customizations/{customization_id}/corpora',
      path: pick(params, ['customization_id']),
      json: true
    },
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.getCorpus"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.SpeechToTextV1.prototype.</span>getCorpus (params, callback)](#apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.getCorpus)
- description and source-code
```javascript
getCorpus = function (params, callback) {
  const parameters = {
    requiredParams: ['customization_id', 'name'],
    options: {
      method: 'GET',
      url: '/v1/customizations/{customization_id}/corpora/{name}',
      path: pick(params, ['customization_id', 'name']),
      json: true
    },
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.getCustomization"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.SpeechToTextV1.prototype.</span>getCustomization (params, callback)](#apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.getCustomization)
- description and source-code
```javascript
getCustomization = function (params, callback) {
  const parameters = {
    requiredParams: ['customization_id'],
    options: {
      method: 'GET',
      url: '/v1/customizations/{customization_id}',
      path: pick(params, ['customization_id']),
      json: true
    },
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.getCustomizations"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.SpeechToTextV1.prototype.</span>getCustomizations (params, callback)](#apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.getCustomizations)
- description and source-code
```javascript
getCustomizations = function (params, callback) {
  if (typeof params === 'function' && !callback) {
    callback = params;
    params = {};
  }
  const parameters = {
    options: {
      method: 'GET',
      url: '/v1/customizations/',
      qs: pick(params, ['language']),
      json: true
    },
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.getModel"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.SpeechToTextV1.prototype.</span>getModel (params, callback)](#apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.getModel)
- description and source-code
```javascript
getModel = function (params, callback) {
  const parameters = {
    requiredParams: ['model_id'],
    options: {
      method: 'GET',
      url: '/v1/models/{model_id}',
      path: pick(params, ['model_id']),
      json: true
    },
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.getModels"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.SpeechToTextV1.prototype.</span>getModels (params, callback)](#apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.getModels)
- description and source-code
```javascript
getModels = function (params, callback) {
  const parameters = {
    options: {
      method: 'GET',
      url: '/v1/models',
      path: params,
      json: true
    },
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.getRecognitionJob"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.SpeechToTextV1.prototype.</span>getRecognitionJob (params, callback)](#apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.getRecognitionJob)
- description and source-code
```javascript
getRecognitionJob = function (params, callback) {
  const missingParams = helper.getMissingParams(params, ['id']);
  if (missingParams) {
    callback(missingParams);
    return;
  }

  const parameters = {
    options: {
      method: 'GET',
      url: '/v1/recognitions/{id}',
      path: pick(params, ['id']),
      json: true
    },
    defaultOptions: this._options
  };

  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.getRecognitionJobs"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.SpeechToTextV1.prototype.</span>getRecognitionJobs (params, callback)](#apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.getRecognitionJobs)
- description and source-code
```javascript
getRecognitionJobs = function (params, callback) {
  if (!callback && typeof params === 'function') {
    callback = params;
  }
  const parameters = {
    options: {
      method: 'GET',
      url: '/v1/recognitions',
      json: true
    },
    defaultOptions: this._options
  };

  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.getRecognizeStatus"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.SpeechToTextV1.prototype.</span>getRecognizeStatus (params, callback)](#apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.getRecognizeStatus)
- description and source-code
```javascript
getRecognizeStatus = function (params, callback) {
  const parameters = {
    requiredParams: ['session_id'],
    options: {
      method: 'GET',
      url: '/v1/sessions/{session_id}/recognize',
      path: pick(params, ['session_id']),
      json: true
    },
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.getWord"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.SpeechToTextV1.prototype.</span>getWord (params, callback)](#apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.getWord)
- description and source-code
```javascript
getWord = function (params, callback) {
  const parameters = {
    requiredParams: ['customization_id', 'word'],
    options: {
      method: 'GET',
      url: '/v1/customizations/{customization_id}/words/{word}',
      path: pick(params, ['customization_id', 'word']),
      json: true
    },
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.getWords"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.SpeechToTextV1.prototype.</span>getWords (params, callback)](#apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.getWords)
- description and source-code
```javascript
getWords = function (params, callback) {
  if (typeof params === 'function' && !callback) {
    callback = params;
    params = {};
  }
  const parameters = {
    requiredParams: ['customization_id'],
    options: {
      method: 'GET',
      url: '/v1/customizations/{customization_id}/words',
      path: pick(params, ['customization_id']),
      qs: pick(params, ['word_type', 'sort']),
      json: true
    },
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.observeResult"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.SpeechToTextV1.prototype.</span>observeResult (params)](#apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.observeResult)
- description and source-code
```javascript
function deprecated(params) {
  if (!(params || {}).silent && !this._options.silent) {
    // eslint-disable-next-line no-console
    console.log(
      new Error(
        'The ${name}() method is deprecated and will be removed from a future version of the watson-developer-cloud SDK. Please
use createRecognizeStream() instead.\n(Set {silent: true} to hide this message.)'
      )
    );
  }
  return original.apply(this, arguments);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.recognize"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.SpeechToTextV1.prototype.</span>recognize (params, callback)](#apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.recognize)
- description and source-code
```javascript
recognize = function (params, callback) {
  const missingParams = helper.getMissingParams(params, ['audio', 'content_type']);
  if (missingParams) {
    callback(missingParams);
    return;
  }
  if (!isStream(params.audio)) {
    callback(new Error('audio is not a standard Node.js Stream'));
    return;
  }

  const queryParams = pick(params, PARAMS_ALLOWED);
  if (Array.isArray(queryParams.keywords)) {
    queryParams.keywords = queryParams.keywords.join(',');
  }

  let _url = '/v1';
  _url += params.session_id ? '/sessions/' + params.session_id : '';
  _url += '/recognize';

  const parameters = {
    options: {
      method: 'POST',
      url: _url,
      headers: {
        'Content-Type': params.content_type
      },
      json: true,
      qs: queryParams
    },
    defaultOptions: this._options
  };
  return params.audio
    .on('response', function(response) {
      // Replace content-type
      response.headers['content-type'] = params.content_type;
    })
    .pipe(requestFactory(parameters, callback));
}
```
- example usage
```shell
...

var params = {
  // From file
  audio: fs.createReadStream('./resources/speech.wav'),
  content_type: 'audio/l16; rate=44100'
};

speech_to_text.recognize(params, function(err, res) {
  if (err)
    console.log(err);
  else
    console.log(JSON.stringify(res, null, 2));
});

// or streaming
...
```

#### <a name="apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.recognizeLive"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.SpeechToTextV1.prototype.</span>recognizeLive (params)](#apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.recognizeLive)
- description and source-code
```javascript
function deprecated(params) {
  if (!(params || {}).silent && !this._options.silent) {
    // eslint-disable-next-line no-console
    console.log(
      new Error(
        'The ${name}() method is deprecated and will be removed from a future version of the watson-developer-cloud SDK. Please
use createRecognizeStream() instead.\n(Set {silent: true} to hide this message.)'
      )
    );
  }
  return original.apply(this, arguments);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.registerCallback"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.SpeechToTextV1.prototype.</span>registerCallback (params, callback)](#apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.registerCallback)
- description and source-code
```javascript
registerCallback = function (params, callback) {
  const missingParams = helper.getMissingParams(params, ['callback_url']);
  if (missingParams) {
    callback(missingParams);
    return;
  }

  const parameters = {
    requiredParams: ['callback_url'],
    options: {
      method: 'POST',
      url: '/v1/register_callback',
      qs: pick(params, ['callback_url', 'user_secret']),
      json: true
    },
    defaultOptions: this._options
  };

  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.resetCustomization"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.SpeechToTextV1.prototype.</span>resetCustomization (params, callback)](#apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.resetCustomization)
- description and source-code
```javascript
resetCustomization = function (params, callback) {
  const parameters = {
    requiredParams: ['customization_id'],
    options: {
      method: 'POST',
      url: '/v1/customizations/{customization_id}/reset',
      path: pick(params, ['customization_id']),
      json: true
    },
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.trainCustomization"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.SpeechToTextV1.prototype.</span>trainCustomization (params, callback)](#apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.trainCustomization)
- description and source-code
```javascript
trainCustomization = function (params, callback) {
  const parameters = {
    requiredParams: ['customization_id'],
    options: {
      method: 'POST',
      url: '/v1/customizations/{customization_id}/train',
      path: pick(params, ['customization_id']),
      qs: pick(params, ['word_type_to_add']),
      json: true
    },
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.whenCorporaAnalyzed"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.SpeechToTextV1.prototype.</span>whenCorporaAnalyzed (params, callback)](#apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.whenCorporaAnalyzed)
- description and source-code
```javascript
whenCorporaAnalyzed = function (params, callback) {
  const self = this;

  async.parallel(
    [
      // validate that it has at least one corpus
      function(next) {
        self.getCorpora(params, function(err, res) {
          if (err) {
            return next(err);
          }
          if (!res.corpora.length) {
            err = new Error('Customization has no corpa and therefore corpus cannot be analyzed');
            err.code = SpeechToTextV1.ERR_NO_CORPORA;
            return next(err);
          }
          next();
        });
      },
      // check the customization status repeatedly until it's available
      function(next) {
        const options = extend(
          {
            interval: 5000,
            times: 30
          },
          params
        );
        options.errorFilter = function(err) {
          // if it's a timeout error, then getCorpora is called again after params.interval
          // otherwise the error is passed back to the user
          // if the params.times limit is reached, the error will be passed to the user regardless
          return err.code === SpeechToTextV1.ERR_TIMEOUT;
        };
        async.retry(
          options,
          function(done) {
            self.getCorpora(params, function(err, corpora) {
              if (err) {
                done(err);
              } else if (isProcessing(corpora)) {
                // if the loop times out, async returns the last error, which will be this one.
                err = new Error('Corpora is still being processed, try increasing interval or times params');
                err.code = SpeechToTextV1.ERR_TIMEOUT;
                done(err);
              } else if (isAnalyzed(corpora)) {
                done(null, corpora);
              } else {
                done(new Error('Unexpected corpus analysis status'));
              }
            });
          },
          next
        );
      }
    ],
    function(err, res) {
      if (err) {
        return callback(err);
      }
      callback(null, res[1]); // callback with the final customization object
    }
  );
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.whenCustomizationReady"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.SpeechToTextV1.prototype.</span>whenCustomizationReady (params, callback)](#apidoc.element.watson-developer-cloud.SpeechToTextV1.prototype.whenCustomizationReady)
- description and source-code
```javascript
whenCustomizationReady = function (params, callback) {
  const self = this;

  // check the customization status repeatedly until it's ready or available

  const options = extend(
    {
      interval: 5000,
      times: 30
    },
    params
  );
  options.errorFilter = function(err) {
    // if it's a timeout error, then getCustomization is called again after params.interval
    // otherwise the error is passed back to the user
    // if the params.times limit is reached, the error will be passed to the user regardless
    return err.code === SpeechToTextV1.ERR_TIMEOUT;
  };
  async.retry(
    options,
    function(next) {
      self.getCustomization(params, function(err, customization) {
        if (err) {
          next(err);
        } else if (customization.status === 'pending' || customization.status === 'training') {
          // if the loop times out, async returns the last error, which will be this one.
          err = new Error('Customization is still pending, try increasing interval or times params');
          err.code = SpeechToTextV1.ERR_TIMEOUT;
          next(err);
        } else if (customization.status === 'ready' || customization.status === 'available') {
          next(null, customization);
        } else if (customization.status === 'failed') {
          next(new Error('Customization training failed'));
        } else {
          next(new Error('Unexpected customization status: ' + customization.status));
        }
      });
    },
    callback
  );
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.watson-developer-cloud.TextToSpeechV1"></a>[module watson-developer-cloud.TextToSpeechV1](#apidoc.module.watson-developer-cloud.TextToSpeechV1)

#### <a name="apidoc.element.watson-developer-cloud.TextToSpeechV1.TextToSpeechV1"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.</span>TextToSpeechV1 (options)](#apidoc.element.watson-developer-cloud.TextToSpeechV1.TextToSpeechV1)
- description and source-code
```javascript
function TextToSpeechV1(options) {
  BaseService.call(this, options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.TextToSpeechV1.super_"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.TextToSpeechV1.</span>super_ (user_options)](#apidoc.element.watson-developer-cloud.TextToSpeechV1.super_)
- description and source-code
```javascript
function BaseService(user_options) {
  if (!(this instanceof BaseService)) {
    // it might be better to just create a new instance and return that.. but that can't be done here, it has to be done in each
 individual service. So this is still a good failsafe even in that case.
    throw new Error('"new" keyword required to create Watson service instances');
  }
  let options = extend({}, user_options);

  options = this.initCredentials(options);

  if (options.url) {
    options.url = helper.stripTrailingSlash(options.url);
  }

  this._options = extend({ qs: {}, url: this.constructor.URL }, this.serviceDefaults, options);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.watson-developer-cloud.TextToSpeechV1.prototype"></a>[module watson-developer-cloud.TextToSpeechV1.prototype](#apidoc.module.watson-developer-cloud.TextToSpeechV1.prototype)

#### <a name="apidoc.element.watson-developer-cloud.TextToSpeechV1.prototype.addWord"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.TextToSpeechV1.prototype.</span>addWord (params, callback)](#apidoc.element.watson-developer-cloud.TextToSpeechV1.prototype.addWord)
- description and source-code
```javascript
addWord = function (params, callback) {
  const parameters = {
    requiredParams: ['customization_id', 'word', 'translation'],
    originalParams: params,
    options: {
      method: 'PUT',
      url: '/v1/customizations/' + params.customization_id + '/words/' + params.word,
      body: pick(params, ['translation']),
      json: true
    },
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.TextToSpeechV1.prototype.addWords"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.TextToSpeechV1.prototype.</span>addWords (params, callback)](#apidoc.element.watson-developer-cloud.TextToSpeechV1.prototype.addWords)
- description and source-code
```javascript
addWords = function (params, callback) {
  const parameters = {
    requiredParams: ['customization_id', 'words'],
    originalParams: params,
    options: {
      method: 'POST',
      url: '/v1/customizations/' + params.customization_id + '/words',
      body: pick(params, ['words']),
      json: true
    },
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.TextToSpeechV1.prototype.createCustomization"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.TextToSpeechV1.prototype.</span>createCustomization (params, callback)](#apidoc.element.watson-developer-cloud.TextToSpeechV1.prototype.createCustomization)
- description and source-code
```javascript
createCustomization = function (params, callback) {
  const parameters = {
    requiredParams: ['name'],
    options: {
      method: 'POST',
      url: '/v1/customizations',
      body: pick(params, ['name', 'language', 'description']),
      json: true
    },
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.TextToSpeechV1.prototype.deleteCustomization"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.TextToSpeechV1.prototype.</span>deleteCustomization (params, callback)](#apidoc.element.watson-developer-cloud.TextToSpeechV1.prototype.deleteCustomization)
- description and source-code
```javascript
deleteCustomization = function (params, callback) {
  const parameters = {
    requiredParams: ['customization_id'],
    originalParams: params,
    options: {
      method: 'DELETE',
      url: '/v1/customizations/' + params.customization_id,
      json: true
    },
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.TextToSpeechV1.prototype.deleteWord"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.TextToSpeechV1.prototype.</span>deleteWord (params, callback)](#apidoc.element.watson-developer-cloud.TextToSpeechV1.prototype.deleteWord)
- description and source-code
```javascript
deleteWord = function (params, callback) {
  const parameters = {
    requiredParams: ['customization_id', 'word'],
    originalParams: params,
    options: {
      method: 'DELETE',
      url: '/v1/customizations/' + params.customization_id + '/words/' + params.word,
      json: true
    },
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.TextToSpeechV1.prototype.getCustomization"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.TextToSpeechV1.prototype.</span>getCustomization (params, callback)](#apidoc.element.watson-developer-cloud.TextToSpeechV1.prototype.getCustomization)
- description and source-code
```javascript
getCustomization = function (params, callback) {
  const parameters = {
    requiredParams: ['customization_id'],
    originalParams: params,
    options: {
      method: 'GET',
      url: '/v1/customizations/' + params.customization_id,
      json: true
    },
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.TextToSpeechV1.prototype.getCustomizations"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.TextToSpeechV1.prototype.</span>getCustomizations (params, callback)](#apidoc.element.watson-developer-cloud.TextToSpeechV1.prototype.getCustomizations)
- description and source-code
```javascript
getCustomizations = function (params, callback) {
  if (typeof params === 'function' && !callback) {
    callback = params;
    params = {};
  }
  const parameters = {
    options: {
      method: 'GET',
      url: '/v1/customizations/',
      qs: pick(params, ['language']),
      json: true
    },
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.TextToSpeechV1.prototype.getWord"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.TextToSpeechV1.prototype.</span>getWord (params, callback)](#apidoc.element.watson-developer-cloud.TextToSpeechV1.prototype.getWord)
- description and source-code
```javascript
getWord = function (params, callback) {
  const parameters = {
    requiredParams: ['customization_id', 'word'],
    originalParams: params,
    options: {
      method: 'GET',
      url: '/v1/customizations/' + params.customization_id + '/words/' + params.word,
      json: true
    },
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.TextToSpeechV1.prototype.getWords"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.TextToSpeechV1.prototype.</span>getWords (params, callback)](#apidoc.element.watson-developer-cloud.TextToSpeechV1.prototype.getWords)
- description and source-code
```javascript
getWords = function (params, callback) {
  if (typeof params === 'function' && !callback) {
    callback = params;
    params = {};
  }
  const parameters = {
    requiredParams: ['customization_id'],
    originalParams: params,
    options: {
      method: 'GET',
      url: '/v1/customizations/' + params.customization_id + '/words',
      json: true
    },
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.TextToSpeechV1.prototype.pronunciation"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.TextToSpeechV1.prototype.</span>pronunciation (params, callback)](#apidoc.element.watson-developer-cloud.TextToSpeechV1.prototype.pronunciation)
- description and source-code
```javascript
pronunciation = function (params, callback) {
  const parameters = {
    requiredParams: ['text'],
    options: {
      method: 'GET',
      url: '/v1/pronunciation',
      qs: pick(params, ['text', 'voice', 'format', 'customization_id']),
      json: true
    },
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.TextToSpeechV1.prototype.synthesize"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.TextToSpeechV1.prototype.</span>synthesize (params, callback)](#apidoc.element.watson-developer-cloud.TextToSpeechV1.prototype.synthesize)
- description and source-code
```javascript
synthesize = function (params, callback) {
  params = extend({ accept: 'audio/ogg; codecs=opus' }, params);

  const parameters = {
    requiredParams: ['text'],
    options: {
      method: 'POST',
      url: '/v1/synthesize',
      body: JSON.stringify(pick(params, ['text'])),
      qs: pick(params, ['accept', 'voice', 'customization_id']),
      path: pick(params, ['text']),
      headers: extend(
        {
          'content-type': 'application/json'
        },
        pick(params, ['X-Watson-Learning-Opt-Out'])
      ),
      encoding: null
    },
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
...
var params = {
  text: 'Hello from IBM Watson',
  voice: 'en-US_AllisonVoice', // Optional voice
  accept: 'audio/wav'
};

// Pipe the synthesized text to a file
text_to_speech.synthesize(params).pipe(fs.createWriteStream('output.wav'));
'''

### Tone Analyzer
Use the [Tone Analyzer][tone_analyzer] service to analyze the
emotion, writing and social tones of a text.

'''js
...
```

#### <a name="apidoc.element.watson-developer-cloud.TextToSpeechV1.prototype.updateCustomization"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.TextToSpeechV1.prototype.</span>updateCustomization (params, callback)](#apidoc.element.watson-developer-cloud.TextToSpeechV1.prototype.updateCustomization)
- description and source-code
```javascript
updateCustomization = function (params, callback) {
  const parameters = {
    requiredParams: ['customization_id', 'words'],
    originalParams: params,
    options: {
      method: 'POST',
      url: '/v1/customizations/' + params.customization_id,
      body: pick(params, ['name', 'description', 'words']),
      json: true
    },
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.TextToSpeechV1.prototype.voice"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.TextToSpeechV1.prototype.</span>voice (params, callback)](#apidoc.element.watson-developer-cloud.TextToSpeechV1.prototype.voice)
- description and source-code
```javascript
voice = function (params, callback) {
  const parameters = {
    requiredParams: ['voice'],
    options: {
      method: 'GET',
      url: '/v1/voices/{voice}',
      path: pick(params, ['voice']),
      qs: pick(params, ['customization_id']),
      json: true
    },
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.TextToSpeechV1.prototype.voices"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.TextToSpeechV1.prototype.</span>voices (params, callback)](#apidoc.element.watson-developer-cloud.TextToSpeechV1.prototype.voices)
- description and source-code
```javascript
voices = function (params, callback) {
  const parameters = {
    options: {
      method: 'GET',
      url: '/v1/voices',
      json: true
    },
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.watson-developer-cloud.ToneAnalyzerV3"></a>[module watson-developer-cloud.ToneAnalyzerV3](#apidoc.module.watson-developer-cloud.ToneAnalyzerV3)

#### <a name="apidoc.element.watson-developer-cloud.ToneAnalyzerV3.ToneAnalyzerV3"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.</span>ToneAnalyzerV3 (options)](#apidoc.element.watson-developer-cloud.ToneAnalyzerV3.ToneAnalyzerV3)
- description and source-code
```javascript
function ToneAnalyzerV3(options) {
  BaseService.call(this, options);
  // Check if 'version_date' was provided
  if (typeof this._options.version_date === 'undefined') {
    throw new Error('Argument error: version_date was not specified, use 2016-05-19');
  }
  // todo: confirm that the service wants version, not version_date
  this._options.qs.version = this._options.version_date;
}
```
- example usage
```shell
...
The following methods will also work, but cause the entire library to be loaded:

'''js
// Alternate methods of using the library.
// Not recommended, especially for client-side JS.
var watson = require('watson-developer-cloud');

var toneAnalyzer = new watson.ToneAnalyzerV3({/*...*/});

var tone_analyzer = watson.tone_analyzer({version: 'v3', /*...*/});
'''

## Installation

'''sh
...
```

#### <a name="apidoc.element.watson-developer-cloud.ToneAnalyzerV3.super_"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.ToneAnalyzerV3.</span>super_ (user_options)](#apidoc.element.watson-developer-cloud.ToneAnalyzerV3.super_)
- description and source-code
```javascript
function BaseService(user_options) {
  if (!(this instanceof BaseService)) {
    // it might be better to just create a new instance and return that.. but that can't be done here, it has to be done in each
 individual service. So this is still a good failsafe even in that case.
    throw new Error('"new" keyword required to create Watson service instances');
  }
  let options = extend({}, user_options);

  options = this.initCredentials(options);

  if (options.url) {
    options.url = helper.stripTrailingSlash(options.url);
  }

  this._options = extend({ qs: {}, url: this.constructor.URL }, this.serviceDefaults, options);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.watson-developer-cloud.ToneAnalyzerV3.prototype"></a>[module watson-developer-cloud.ToneAnalyzerV3.prototype](#apidoc.module.watson-developer-cloud.ToneAnalyzerV3.prototype)

#### <a name="apidoc.element.watson-developer-cloud.ToneAnalyzerV3.prototype.tone"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.ToneAnalyzerV3.prototype.</span>tone (params, callback)](#apidoc.element.watson-developer-cloud.ToneAnalyzerV3.prototype.tone)
- description and source-code
```javascript
tone = function (params, callback) {
  if (!params || !params.text) {
    callback(new Error('Missing required parameters: text'));
    return;
  }
  const contentType = params.isHTML ? 'text/html' : 'text/plain';
  const parameters = {
    options: {
      url: '/v3/tone',
      method: 'POST',
      body: params.text,
      qs: pick(params, ['tones', 'sentences'])
    },
    defaultOptions: extend(true, this._options, {
      headers: {
        accept: 'application/json',
        'content-type': contentType
      }
    })
  };

  return requestFactory(parameters, callback);
}
```
- example usage
```shell
...

var tone_analyzer = new ToneAnalyzerV3({
  username: '<username>',
  password: '<password>',
  version_date: '2016-05-19'
});

tone_analyzer.tone({ text: 'Greetings from Watson Developer Cloud!' },
  function(err, tone) {
    if (err)
      console.log(err);
    else
      console.log(JSON.stringify(tone, null, 2));
});
'''
...
```



# <a name="apidoc.module.watson-developer-cloud.TradeoffAnalyticsV1"></a>[module watson-developer-cloud.TradeoffAnalyticsV1](#apidoc.module.watson-developer-cloud.TradeoffAnalyticsV1)

#### <a name="apidoc.element.watson-developer-cloud.TradeoffAnalyticsV1.TradeoffAnalyticsV1"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.</span>TradeoffAnalyticsV1 (options)](#apidoc.element.watson-developer-cloud.TradeoffAnalyticsV1.TradeoffAnalyticsV1)
- description and source-code
```javascript
function TradeoffAnalyticsV1(options) {
  BaseService.call(this, options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.TradeoffAnalyticsV1.super_"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.TradeoffAnalyticsV1.</span>super_ (user_options)](#apidoc.element.watson-developer-cloud.TradeoffAnalyticsV1.super_)
- description and source-code
```javascript
function BaseService(user_options) {
  if (!(this instanceof BaseService)) {
    // it might be better to just create a new instance and return that.. but that can't be done here, it has to be done in each
 individual service. So this is still a good failsafe even in that case.
    throw new Error('"new" keyword required to create Watson service instances');
  }
  let options = extend({}, user_options);

  options = this.initCredentials(options);

  if (options.url) {
    options.url = helper.stripTrailingSlash(options.url);
  }

  this._options = extend({ qs: {}, url: this.constructor.URL }, this.serviceDefaults, options);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.watson-developer-cloud.TradeoffAnalyticsV1.prototype"></a>[module watson-developer-cloud.TradeoffAnalyticsV1.prototype](#apidoc.module.watson-developer-cloud.TradeoffAnalyticsV1.prototype)

#### <a name="apidoc.element.watson-developer-cloud.TradeoffAnalyticsV1.prototype.dilemmas"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.TradeoffAnalyticsV1.prototype.</span>dilemmas (params, callback)](#apidoc.element.watson-developer-cloud.TradeoffAnalyticsV1.prototype.dilemmas)
- description and source-code
```javascript
dilemmas = function (params, callback) {
  params = params || {};
  const qs = {};
  if (params.find_preferable_options) {
    qs.find_preferable_options = true;
  }
  if (params.generate_visualization === false) {
    qs.generate_visualization = false;
  }
  const parameters = {
    options: {
      method: 'POST',
      url: '/v1/dilemmas',
      body: omit(params, ['metadata_header', 'generate_visualization', 'find_preferable_options']),
      headers: {
        'x-watson-metadata': params.metadata_header
      },
      qs: qs,
      json: true
    },
    requiredParams: ['columns', 'subject', 'options'],
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
...
  username: '<username>',
  password: '<password>'
});

// From file
var params = require('./resources/problem.json');

tradeoff_analytics.dilemmas(params, function(err, res) {
  if (err)
    console.log(err);
  else
    console.log(JSON.stringify(res, null, 2));
});
'''
...
```

#### <a name="apidoc.element.watson-developer-cloud.TradeoffAnalyticsV1.prototype.events"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.TradeoffAnalyticsV1.prototype.</span>events (params, callback)](#apidoc.element.watson-developer-cloud.TradeoffAnalyticsV1.prototype.events)
- description and source-code
```javascript
events = function (params, callback) {
  params = params || {};

  const parameters = {
    options: {
      method: 'POST',
      url: '/v1/events',
      body: omit(params, ['metadata_header', 'generate_visualization']),
      headers: {
        'x-watson-metadata': params.metadata_header
      },
      json: true
    },
    defaultOptions: this._options
  };
  return requestFactory(parameters, callback);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.watson-developer-cloud.VisualRecognitionV3"></a>[module watson-developer-cloud.VisualRecognitionV3](#apidoc.module.watson-developer-cloud.VisualRecognitionV3)

#### <a name="apidoc.element.watson-developer-cloud.VisualRecognitionV3.VisualRecognitionV3"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.</span>VisualRecognitionV3 (options)](#apidoc.element.watson-developer-cloud.VisualRecognitionV3.VisualRecognitionV3)
- description and source-code
```javascript
function VisualRecognitionV3(options) {
  BaseService.call(this, options);
  // Check if 'version_date' was provided
  if (typeof this._options.version_date === 'undefined') {
    throw new Error('Argument error: version_date was not specified, use 2016-05-20');
  }
  this._options.qs.version = this._options.version_date; // todo: confirm service expects version not version_date
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.VisualRecognitionV3.super_"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.VisualRecognitionV3.</span>super_ (user_options)](#apidoc.element.watson-developer-cloud.VisualRecognitionV3.super_)
- description and source-code
```javascript
function BaseService(user_options) {
  if (!(this instanceof BaseService)) {
    // it might be better to just create a new instance and return that.. but that can't be done here, it has to be done in each
 individual service. So this is still a good failsafe even in that case.
    throw new Error('"new" keyword required to create Watson service instances');
  }
  let options = extend({}, user_options);

  options = this.initCredentials(options);

  if (options.url) {
    options.url = helper.stripTrailingSlash(options.url);
  }

  this._options = extend({ qs: {}, url: this.constructor.URL }, this.serviceDefaults, options);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.watson-developer-cloud.VisualRecognitionV3.prototype"></a>[module watson-developer-cloud.VisualRecognitionV3.prototype](#apidoc.module.watson-developer-cloud.VisualRecognitionV3.prototype)

#### <a name="apidoc.element.watson-developer-cloud.VisualRecognitionV3.prototype.addImage"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.VisualRecognitionV3.prototype.</span>addImage (params, callback)](#apidoc.element.watson-developer-cloud.VisualRecognitionV3.prototype.addImage)
- description and source-code
```javascript
addImage = function (params, callback) {
  params = params || {};

  if (!params.image_file || !isStream(params.image_file)) {
    throw new Error('image_file param must be a standard Node.js Stream');
  }

  const parameters = {
    options: {
      url: '/v3/collections/{collection_id}/images',
      method: 'POST',
      json: true,
      path: params,
      formData: {
        image_file: params.image_file,
        metadata: {
          value: JSON.stringify(params.metadata || {}),
          options: {
            contentType: 'application/json',
            filename: 'metadata.json' // it doesn't matter what the filename is, but the service requires that *some* filename be
 set or else it ignores the metadata
          }
        }
      }
    },
    requiredParams: ['collection_id', 'image_file'],
    defaultOptions: this._options
  };
  return this.request(parameters, errorFormatter(callback));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.VisualRecognitionV3.prototype.classify"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.VisualRecognitionV3.prototype.</span>classify (params, callback)](#apidoc.element.watson-developer-cloud.VisualRecognitionV3.prototype.classify)
- description and source-code
```javascript
classify = function (params, callback) {
  try {
    fixupImageParam(params);
  } catch (e) {
    callback(e);
    return;
  }

  params = extend(
    {
      classifier_ids: ['default'],
      owners: ['me', 'IBM']
    },
    params
  );

  let parameters;

  if (params.images_file) {
    parameters = {
      options: {
        url: '/v3/classify',
        method: 'POST',
        formData: {
          images_file: params.images_file,
          parameters: {
            value: JSON.stringify(pick(params, ['classifier_ids', 'owners', 'threshold'])),
            options: {
              contentType: 'application/json'
            }
          }
        },
        headers: pick(params, 'Accept-Language')
      },
      defaultOptions: this._options
    };
  } else {
    parameters = {
      options: {
        url: '/v3/classify',
        method: 'GET',
        json: true,
        qs: pick(params, ['url', 'classifier_ids', 'owners', 'threshold']),
        headers: pick(params, 'Accept-Language')
      },
      defaultOptions: this._options
    };
  }

  return this.request(parameters, errorFormatter(callback));
}
```
- example usage
```shell
...
var NaturalLanguageClassifierV1 = require('watson-developer-cloud/natural-language-classifier/v1');

var natural_language_classifier = new NaturalLanguageClassifierV1({
username: '<username>',
password: '<password>'
});

natural_language_classifier.classify({
text: 'Is it sunny?',
classifier_id: '<classifier-id>' },
function(err, response) {
  if (err)
    console.log('error:', err);
  else
    console.log(JSON.stringify(response, null, 2));
...
```

#### <a name="apidoc.element.watson-developer-cloud.VisualRecognitionV3.prototype.createClassifier"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.VisualRecognitionV3.prototype.</span>createClassifier (params, callback)](#apidoc.element.watson-developer-cloud.VisualRecognitionV3.prototype.createClassifier)
- description and source-code
```javascript
createClassifier = function (params, callback) {
  params = params || {};

  const example_keys = Object.keys(params).filter(function(key) {
    return key === NEGATIVE_EXAMPLES || key.match(/^.+_positive_examples$/);
  });

  if (example_keys.length < 2) {
    callback(new Error('Missing required parameters: either two *_positive_examples or one *_positive_examples and one negative_examples
 must be provided.'));
    return;
  }
  // todo: validate that all *_examples are streams or else objects with buffers and content-types
  const allowed_keys = ['name', NEGATIVE_EXAMPLES].concat(example_keys);

  const parameters = {
    options: {
      url: '/v3/classifiers',
      method: 'POST',
      json: true,
      formData: pick(params, allowed_keys)
    },
    requiredParams: ['name'],
    defaultOptions: this._options
  };
  return this.request(parameters, errorFormatter(callback));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.VisualRecognitionV3.prototype.createCollection"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.VisualRecognitionV3.prototype.</span>createCollection (params, callback)](#apidoc.element.watson-developer-cloud.VisualRecognitionV3.prototype.createCollection)
- description and source-code
```javascript
createCollection = function (params, callback) {
  params = params || {};

  const parameters = {
    options: {
      url: '/v3/collections',
      method: 'POST',
      json: true,
      formData: pick(params, ['name'])
    },
    requiredParams: ['name'],
    defaultOptions: this._options
  };
  return this.request(parameters, errorFormatter(callback));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.VisualRecognitionV3.prototype.deleteClassifier"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.VisualRecognitionV3.prototype.</span>deleteClassifier (params, callback)](#apidoc.element.watson-developer-cloud.VisualRecognitionV3.prototype.deleteClassifier)
- description and source-code
```javascript
deleteClassifier = function (params, callback) {
  const parameters = {
    options: {
      method: 'DELETE',
      url: '/v3/classifiers/{classifier_id}',
      path: params,
      json: true
    },
    requiredParams: ['classifier_id'],
    defaultOptions: this._options
  };
  return this.request(parameters, errorFormatter(callback));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.VisualRecognitionV3.prototype.deleteCollection"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.VisualRecognitionV3.prototype.</span>deleteCollection (params, callback)](#apidoc.element.watson-developer-cloud.VisualRecognitionV3.prototype.deleteCollection)
- description and source-code
```javascript
deleteCollection = function (params, callback) {
  params = params || {};

  const parameters = {
    options: {
      url: '/v3/collections/{collection_id}',
      method: 'DELETE',
      json: true,
      path: params
    },
    requiredParams: ['collection_id'],
    defaultOptions: this._options
  };
  return this.request(parameters, errorFormatter(callback));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.VisualRecognitionV3.prototype.deleteImage"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.VisualRecognitionV3.prototype.</span>deleteImage (params, callback)](#apidoc.element.watson-developer-cloud.VisualRecognitionV3.prototype.deleteImage)
- description and source-code
```javascript
deleteImage = function (params, callback) {
  params = params || {};

  const parameters = {
    options: {
      url: '/v3/collections/{collection_id}/images/{image_id}',
      method: 'DELETE',
      json: true,
      path: params
    },
    requiredParams: ['collection_id', 'image_id'],
    defaultOptions: this._options
  };
  return this.request(parameters, errorFormatter(callback));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.VisualRecognitionV3.prototype.deleteImageMetadata"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.VisualRecognitionV3.prototype.</span>deleteImageMetadata (params, callback)](#apidoc.element.watson-developer-cloud.VisualRecognitionV3.prototype.deleteImageMetadata)
- description and source-code
```javascript
deleteImageMetadata = function (params, callback) {
  params = params || {};

  const parameters = {
    options: {
      url: '/v3/collections/{collection_id}/images/{image_id}/metadata',
      method: 'DELETE',
      json: true,
      path: params
    },
    requiredParams: ['collection_id', 'image_id'],
    defaultOptions: this._options
  };
  return this.request(parameters, errorFormatter(callback));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.VisualRecognitionV3.prototype.detectFaces"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.VisualRecognitionV3.prototype.</span>detectFaces (params, callback)](#apidoc.element.watson-developer-cloud.VisualRecognitionV3.prototype.detectFaces)
- description and source-code
```javascript
detectFaces = function (params, callback) {
  try {
    fixupImageParam(params);
  } catch (e) {
    callback(e);
    return;
  }

  let parameters;

  if (params.images_file) {
    parameters = {
      options: {
        url: '/v3/detect_faces',
        method: 'POST',
        json: true,
        formData: pick(params, ['images_file'])
      },
      defaultOptions: this._options
    };
  } else {
    parameters = {
      options: {
        url: '/v3/detect_faces',
        method: 'GET',
        json: true,
        qs: pick(params, ['url'])
      },
      defaultOptions: this._options
    };
  }

  return this.request(parameters, errorFormatter(callback));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.VisualRecognitionV3.prototype.findSimilar"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.VisualRecognitionV3.prototype.</span>findSimilar (params, callback)](#apidoc.element.watson-developer-cloud.VisualRecognitionV3.prototype.findSimilar)
- description and source-code
```javascript
findSimilar = function (params, callback) {
  params = params || {};

  if (!params.image_file || !isStream(params.image_file)) {
    throw new Error('image_file param must be a standard Node.js Stream');
  }

  const parameters = {
    options: {
      url: '/v3/collections/{collection_id}/find_similar',
      method: 'POST',
      json: true,
      qs: pick(params, ['limit']),
      formData: pick(params, ['image_file']),
      path: pick(params, ['collection_id'])
    },
    requiredParams: ['collection_id', 'image_file'],
    defaultOptions: this._options
  };
  return this.request(parameters, errorFormatter(callback));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.VisualRecognitionV3.prototype.getClassifier"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.VisualRecognitionV3.prototype.</span>getClassifier (params, callback)](#apidoc.element.watson-developer-cloud.VisualRecognitionV3.prototype.getClassifier)
- description and source-code
```javascript
getClassifier = function (params, callback) {
  const parameters = {
    options: {
      method: 'GET',
      url: '/v3/classifiers/{classifier_id}',
      path: params,
      json: true
    },
    requiredParams: ['classifier_id'],
    defaultOptions: this._options
  };
  return this.request(parameters, errorFormatter(callback));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.VisualRecognitionV3.prototype.getCollection"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.VisualRecognitionV3.prototype.</span>getCollection (params, callback)](#apidoc.element.watson-developer-cloud.VisualRecognitionV3.prototype.getCollection)
- description and source-code
```javascript
getCollection = function (params, callback) {
  params = params || {};

  const parameters = {
    options: {
      url: '/v3/collections/{collection_id}',
      method: 'GET',
      json: true,
      path: params
    },
    requiredParams: ['collection_id'],
    defaultOptions: this._options
  };
  return this.request(parameters, errorFormatter(callback));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.VisualRecognitionV3.prototype.getCredentialsFromBluemix"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.VisualRecognitionV3.prototype.</span>getCredentialsFromBluemix ()](#apidoc.element.watson-developer-cloud.VisualRecognitionV3.prototype.getCredentialsFromBluemix)
- description and source-code
```javascript
getCredentialsFromBluemix = function () {
  return BaseService.prototype.getCredentialsFromBluemix.call(this, 'watson_vision_combined');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.VisualRecognitionV3.prototype.getCredentialsFromEnvironment"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.VisualRecognitionV3.prototype.</span>getCredentialsFromEnvironment (name)](#apidoc.element.watson-developer-cloud.VisualRecognitionV3.prototype.getCredentialsFromEnvironment)
- description and source-code
```javascript
getCredentialsFromEnvironment = function (name) {
  return {
    api_key: process.env[name.toUpperCase() + '_API_KEY'],
    url: process.env[name + '_URL']
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.VisualRecognitionV3.prototype.getImage"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.VisualRecognitionV3.prototype.</span>getImage (params, callback)](#apidoc.element.watson-developer-cloud.VisualRecognitionV3.prototype.getImage)
- description and source-code
```javascript
getImage = function (params, callback) {
  params = params || {};

  const parameters = {
    options: {
      url: '/v3/collections/{collection_id}/images/{image_id}',
      method: 'GET',
      json: true,
      path: params
    },
    requiredParams: ['collection_id', 'image_id'],
    defaultOptions: this._options
  };
  return this.request(parameters, errorFormatter(callback));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.VisualRecognitionV3.prototype.getImageMetadata"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.VisualRecognitionV3.prototype.</span>getImageMetadata (params, callback)](#apidoc.element.watson-developer-cloud.VisualRecognitionV3.prototype.getImageMetadata)
- description and source-code
```javascript
getImageMetadata = function (params, callback) {
  params = params || {};

  const parameters = {
    options: {
      url: '/v3/collections/{collection_id}/images/{image_id}/metadata',
      method: 'GET',
      json: true,
      path: params
    },
    requiredParams: ['collection_id', 'image_id'],
    defaultOptions: this._options
  };
  return this.request(parameters, errorFormatter(callback));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.VisualRecognitionV3.prototype.initCredentials"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.VisualRecognitionV3.prototype.</span>initCredentials (options)](#apidoc.element.watson-developer-cloud.VisualRecognitionV3.prototype.initCredentials)
- description and source-code
```javascript
initCredentials = function (options) {
  options.api_key = options.api_key || options.apikey;
  options = extend(
    {},
    this.getCredentialsFromBluemix(this.name), // todo: test if this works
    this.getCredentialsFromEnvironment(this.name),
    options
  );
  if (!options.use_unauthenticated) {
    if (!options.api_key) {
      throw new Error('Argument error: api_key was not specified');
    }
    // Per documentation, Alchemy* services use 'apikey', but Visual Recognition uses ('api_key')
    // (Either will work in most cases, but the VR Collections & Similarity Search beta only supports 'api_key')
    options.qs = extend({ api_key: options.api_key }, options.qs);
  }
  return options;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.VisualRecognitionV3.prototype.listClassifiers"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.VisualRecognitionV3.prototype.</span>listClassifiers (params, callback)](#apidoc.element.watson-developer-cloud.VisualRecognitionV3.prototype.listClassifiers)
- description and source-code
```javascript
listClassifiers = function (params, callback) {
  const parameters = {
    options: {
      method: 'GET',
      url: '/v3/classifiers',
      qs: pick(params, ['verbose']),
      json: true
    },
    defaultOptions: this._options
  };
  return this.request(parameters, errorFormatter(callback));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.VisualRecognitionV3.prototype.listCollections"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.VisualRecognitionV3.prototype.</span>listCollections (params, callback)](#apidoc.element.watson-developer-cloud.VisualRecognitionV3.prototype.listCollections)
- description and source-code
```javascript
listCollections = function (params, callback) {
  if (typeof params === 'function' && !callback) {
    callback = params;
  }

  const parameters = {
    options: {
      url: '/v3/collections',
      method: 'GET',
      json: true
    },
    defaultOptions: this._options
  };
  return this.request(parameters, errorFormatter(callback));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.VisualRecognitionV3.prototype.listImages"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.VisualRecognitionV3.prototype.</span>listImages (params, callback)](#apidoc.element.watson-developer-cloud.VisualRecognitionV3.prototype.listImages)
- description and source-code
```javascript
listImages = function (params, callback) {
  params = params || {};

  const parameters = {
    options: {
      url: '/v3/collections/{collection_id}/images',
      method: 'GET',
      json: true,
      path: params
    },
    requiredParams: ['collection_id'],
    defaultOptions: this._options
  };
  return this.request(parameters, errorFormatter(callback));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.VisualRecognitionV3.prototype.recognizeText"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.VisualRecognitionV3.prototype.</span>recognizeText (params, callback)](#apidoc.element.watson-developer-cloud.VisualRecognitionV3.prototype.recognizeText)
- description and source-code
```javascript
recognizeText = function (params, callback) {
  try {
    fixupImageParam(params);
  } catch (e) {
    callback(e);
    return;
  }

  let parameters;

  if (params.images_file) {
    parameters = {
      options: {
        url: '/v3/recognize_text',
        method: 'POST',
        json: true,
        formData: pick(params, ['images_file'])
      },
      defaultOptions: this._options
    };
  } else {
    parameters = {
      options: {
        url: '/v3/recognize_text',
        method: 'GET',
        json: true,
        qs: pick(params, ['url'])
      },
      defaultOptions: this._options
    };
  }

  return this.request(parameters, errorFormatter(callback));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.VisualRecognitionV3.prototype.request"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.VisualRecognitionV3.prototype.</span>request (parameters, cb)](#apidoc.element.watson-developer-cloud.VisualRecognitionV3.prototype.request)
- description and source-code
```javascript
request = function (parameters, cb) {
  const qs = parameters.options.qs;
  if (qs) {
    // array params are turned into a comma-separated string when in querystrings
    Object.keys(qs).forEach(k => Array.isArray(qs[k]) && (qs[k] = qs[k].join(',')));
  }
  return requestFactory(parameters, cb);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.VisualRecognitionV3.prototype.retrainClassifier"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.VisualRecognitionV3.prototype.</span>retrainClassifier (params, callback)](#apidoc.element.watson-developer-cloud.VisualRecognitionV3.prototype.retrainClassifier)
- description and source-code
```javascript
retrainClassifier = function (params, callback) {
  params = params || {};

  const allowed_keys = Object.keys(params).filter(function(key) {
    return key === NEGATIVE_EXAMPLES || key.match(/^.+_positive_examples$/);
  });

  const parameters = {
    options: {
      url: '/v3/classifiers/' + params.classifier_id,
      method: 'POST',
      json: true,
      formData: pick(params, allowed_keys)
    },
    requiredParams: [],
    defaultOptions: this._options
  };
  return this.request(parameters, errorFormatter(callback));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.VisualRecognitionV3.prototype.setImageMetadata"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.VisualRecognitionV3.prototype.</span>setImageMetadata (params, callback)](#apidoc.element.watson-developer-cloud.VisualRecognitionV3.prototype.setImageMetadata)
- description and source-code
```javascript
setImageMetadata = function (params, callback) {
  params = params || {};

  const parameters = {
    options: {
      url: '/v3/collections/{collection_id}/images/{image_id}/metadata',
      method: 'PUT',
      json: true,
      path: params,
      headers: { 'Content-Type': 'multipart/form-data' },
      // todo: manually create a body string that looks like a POST form data body even though it's a PUT
      formData: {
        metadata: {
          value: JSON.stringify(params.metadata || {}),
          options: {
            contentType: 'application/json',
            filename: 'metadata.json' // it doesn't matter what the filename is, but the service requires that *some* filename be
 set or else it gives a confusing "Missing multipart/form-data" error
          }
        }
      }
    },
    requiredParams: ['collection_id', 'image_id', 'metadata'],
    defaultOptions: this._options
  };
  return this.request(parameters, errorFormatter(callback));
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.watson-developer-cloud.helper"></a>[module watson-developer-cloud.helper](#apidoc.module.watson-developer-cloud.helper)

#### <a name="apidoc.element.watson-developer-cloud.helper.getFormat"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.helper.</span>getFormat (params, formats)](#apidoc.element.watson-developer-cloud.helper.getFormat)
- description and source-code
```javascript
getFormat = function (params, formats) {
  if (!formats || !params) {
    return null;
  }

  for (let i = 0; i < formats.length; i++) {
    if (formats[i] in params) {
      return formats[i];
    }
  }
  return null;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.helper.getMissingParams"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.helper.</span>getMissingParams (params, requires)](#apidoc.element.watson-developer-cloud.helper.getMissingParams)
- description and source-code
```javascript
getMissingParams = function (params, requires) {
  let missing;

  if (!requires) {
    return null;
  } else if (!params) {
    missing = requires;
  } else {
    missing = [];

    requires.forEach(function(require) {
      if (!params[require]) {
        missing.push(require);
      }
    });
  }

  return missing.length > 0 ? new Error('Missing required parameters: ' + missing.join(', ')) : null;
}
```
- example usage
```shell
...

// Missing parameters
if (parameters.options.requiredParams) {
  // eslint-disable-next-line no-console
  console.warn(new Error('requiredParams set on parameters.options - it should be set directly on parameters'));
}

missingParams = helper.getMissingParams(parameters.originalParams || extend({}, qs, body, form, formData, path), parameters.requiredParams
);

if (missingParams) {
  if (typeof _callback === 'function') {
    return callback(missingParams);
  } else {
    const errorStream = readableStream();
    setTimeout(
...
```

#### <a name="apidoc.element.watson-developer-cloud.helper.isHTML"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.helper.</span>isHTML (text)](#apidoc.element.watson-developer-cloud.helper.isHTML)
- description and source-code
```javascript
isHTML = function (text) {
  return /<[a-z][\s\S]*>/i.test(text);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.helper.stripTrailingSlash"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.helper.</span>stripTrailingSlash (url)](#apidoc.element.watson-developer-cloud.helper.stripTrailingSlash)
- description and source-code
```javascript
stripTrailingSlash = function (url) {
  // Match a forward slash / at the end of the string ($)
  return url.replace(/\/$/, '');
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.watson-developer-cloud.recognize_stream"></a>[module watson-developer-cloud.recognize_stream](#apidoc.module.watson-developer-cloud.recognize_stream)

#### <a name="apidoc.element.watson-developer-cloud.recognize_stream.recognize_stream"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.</span>recognize_stream (options)](#apidoc.element.watson-developer-cloud.recognize_stream.recognize_stream)
- description and source-code
```javascript
function RecognizeStream(options) {
  Duplex.call(this, options);
  this.options = options;
  this.listening = false;
  this.initialized = false;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.recognize_stream.getContentType"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.recognize_stream.</span>getContentType (buffer)](#apidoc.element.watson-developer-cloud.recognize_stream.getContentType)
- description and source-code
```javascript
getContentType = function (buffer) {
  const header = buffer.slice(0, 4).toString();
  return headerToContentType[header];
}
```
- example usage
```shell
...
const self = this;
if (self.listening) {
  self.socket.send(chunk);
  this.afterSend(callback);
} else {
  if (!this.initialized) {
    if (!this.options['content-type']) {
      this.options['content-type'] = RecognizeStream.getContentType(chunk);
    }
    this.initialize();
  }
  this.once('listening', function() {
    self.socket.send(chunk);
    self.afterSend(callback);
  });
...
```

#### <a name="apidoc.element.watson-developer-cloud.recognize_stream.super_"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.recognize_stream.</span>super_ (options)](#apidoc.element.watson-developer-cloud.recognize_stream.super_)
- description and source-code
```javascript
function Duplex(options) {
  if (!(this instanceof Duplex))
    return new Duplex(options);

  Readable.call(this, options);
  Writable.call(this, options);

  if (options && options.readable === false)
    this.readable = false;

  if (options && options.writable === false)
    this.writable = false;

  this.allowHalfOpen = true;
  if (options && options.allowHalfOpen === false)
    this.allowHalfOpen = false;

  this.once('end', onend);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.watson-developer-cloud.recognize_stream.prototype"></a>[module watson-developer-cloud.recognize_stream.prototype](#apidoc.module.watson-developer-cloud.recognize_stream.prototype)

#### <a name="apidoc.element.watson-developer-cloud.recognize_stream.prototype._read"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.recognize_stream.prototype.</span>_read ()](#apidoc.element.watson-developer-cloud.recognize_stream.prototype._read)
- description and source-code
```javascript
_read = function () /* size*/ {
  // there's no easy way to control reads from the underlying library
  // so, the best we can do here is a no-op
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.recognize_stream.prototype._write"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.recognize_stream.prototype.</span>_write (chunk, encoding, callback)](#apidoc.element.watson-developer-cloud.recognize_stream.prototype._write)
- description and source-code
```javascript
_write = function (chunk, encoding, callback) {
  const self = this;
  if (self.listening) {
    self.socket.send(chunk);
    this.afterSend(callback);
  } else {
    if (!this.initialized) {
      if (!this.options['content-type']) {
        this.options['content-type'] = RecognizeStream.getContentType(chunk);
      }
      this.initialize();
    }
    this.once('listening', function() {
      self.socket.send(chunk);
      self.afterSend(callback);
    });
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.recognize_stream.prototype.afterSend"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.recognize_stream.prototype.</span>afterSend (next)](#apidoc.element.watson-developer-cloud.recognize_stream.prototype.afterSend)
- description and source-code
```javascript
function afterSend(next) {
  // note: bufferedAmount is currently always 0
  // see https://github.com/theturtle32/WebSocket-Node/issues/243
  if (this.socket.bufferedAmount <= (this._writableState.highWaterMark || 0)) {
    process.nextTick(next);
  } else {
    setTimeout(this.afterSend.bind(this, next), 10);
  }
}
```
- example usage
```shell
...
// so, the best we can do here is a no-op
};

RecognizeStream.prototype._write = function(chunk, encoding, callback) {
const self = this;
if (self.listening) {
  self.socket.send(chunk);
  this.afterSend(callback);
} else {
  if (!this.initialized) {
    if (!this.options['content-type']) {
      this.options['content-type'] = RecognizeStream.getContentType(chunk);
    }
    this.initialize();
  }
...
```

#### <a name="apidoc.element.watson-developer-cloud.recognize_stream.prototype.getTransactionId"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.recognize_stream.prototype.</span>getTransactionId ()](#apidoc.element.watson-developer-cloud.recognize_stream.prototype.getTransactionId)
- description and source-code
```javascript
getTransactionId = function () {
  if (this.socket && this.socket._client && this.socket._client.response && this.socket._client.response.headers) {
    return Promise.resolve(this.socket._client.response.headers['x-global-transaction-id']);
  } else {
    return new Promise((resolve, reject) => {
      this.on('connect', () => {
        resolve(this.socket._client.response.headers['x-global-transaction-id']);
      });
      this.on('error', reject);
    });
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.watson-developer-cloud.recognize_stream.prototype.initialize"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.recognize_stream.prototype.</span>initialize ()](#apidoc.element.watson-developer-cloud.recognize_stream.prototype.initialize)
- description and source-code
```javascript
initialize = function () {
  const options = this.options;

  // todo: apply these corrections to other methods (?)
  if (options.token && !options['watson-token']) {
    options['watson-token'] = options.token;
  }
  if (options.content_type && !options['content-type']) {
    options['content-type'] = options.content_type;
  }
  if (options['X-WDC-PL-OPT-OUT'] && !options['X-Watson-Learning-Opt-Out']) {
    options['X-Watson-Learning-Opt-Out'] = options['X-WDC-PL-OPT-OUT'];
  }

  const queryParams = extend({ model: 'en-US_BroadbandModel' }, pick(options, QUERY_PARAMS_ALLOWED));
  const queryString = Object.keys(queryParams)
    .map(function(key) {
      return key + '=' + (key === 'watson-token' ? queryParams[key] : encodeURIComponent(queryParams[key])); // our server chokes
 if the token is correctly url-encoded
    })
    .join('&');

  const url = (options.url || 'wss://stream.watsonplatform.net/speech-to-text/api').replace(/^http/, 'ws') + '/v1/recognize?' +
queryString;

  const openingMessage = extend(
    {
      action: 'start',
      'content-type': 'audio/wav',
      continuous: true,
      interim_results: true,
      word_confidence: true,
      timestamps: true,
      max_alternatives: 3,
      inactivity_timeout: 600
    },
    pick(options, OPENING_MESSAGE_PARAMS_ALLOWED)
  );

  const closingMessage = { action: 'stop' };

  const self = this;

  // node params: requestUrl, protocols, origin, headers, extraRequestOptions
  // browser params: requestUrl, protocols (all others ignored)
  const socket = this.socket = new W3CWebSocket(url, null, null, options.headers, null);

  // when the input stops, let the service know that we're done
  self.on('finish', function() {
    if (self.socket && self.socket.readyState === W3CWebSocket.OPEN) {
      self.socket.send(JSON.stringify(closingMessage));
    } else {
      self.once('connect', function() {
        self.socket.send(JSON.stringify(closingMessage));
      });
    }
  });

  socket.onerror = function(error) {
    self.listening = false;
    self.emit('error', error);
  };

  this.socket.onopen = function() {
    socket.send(JSON.stringify(openingMessage));
    self.emit('connect');
  };

  this.socket.onclose = function(e) {
    self.listening = false;
    self.push(null);
<span class="apidocCodeCommentSpan">    /**
     * @event RecognizeStream#close
     * @param {Number} reasonCode
     * @param {String} description
     */
</span>    self.emit('close', e.code, e.reason);
  };

  /**
   * @event RecognizeStream#error
   */
  function emitError(msg, frame, err) {
    if (err) {
      err.message = msg + ' ' + err.message;
    } else {
      err = new Error(msg);
    }
    err.raw = frame;
    self.emit('error', err);
  }

  socket.onmessage = function(frame) {
    if (typeof frame.data !== 'string') {
      return emitError('Unexpected binary data received from server', frame);
    }

    let data;
    try {
      data = JSON.parse(frame.data);
    } catch (jsonEx) {
      return emitError('Invalid JSON received from service:', frame, jsonEx);
    }

    let recognized = false;
    if (data.error) {
      emitError(data.error, frame);
      recognized = true;
    }

    if (data.state === 'listening') {
      // this is emitted both when the server is ready for audio, and after we send the close message to indicate that it's done
 processing
      if (!self.listening) {
        self.listening = true;
        self.emit('listening');
      } else {
        self.listening = false;
        socket.close();
      }
      recognized = true;
    }

    if (data.results) {
      /**
       * Object with interim or final results, including possible alternatives. May have no results at all for empty audio files
.
       * @event RecognizeStream#results
       * @param {Object} results
       */
      self.emit('results', data);
      // note: currently there is always either no entries or exactly 1 entry in the results array. However, this may change in
the future.
      if (data.results[0] && data.results[0].final && data.results[0].alternatives) {
        /**
         * Finalized text
         * @event RecognizeS ...
```
- example usage
```shell
...
    self.socket.send(chunk);
    this.afterSend(callback);
  } else {
    if (!this.initialized) {
      if (!this.options['content-type']) {
        this.options['content-type'] = RecognizeStream.getContentType(chunk);
      }
      this.initialize();
    }
    this.once('listening', function() {
      self.socket.send(chunk);
      self.afterSend(callback);
    });
  }
};
...
```

#### <a name="apidoc.element.watson-developer-cloud.recognize_stream.prototype.stop"></a>[function <span class="apidocSignatureSpan">watson-developer-cloud.recognize_stream.prototype.</span>stop ()](#apidoc.element.watson-developer-cloud.recognize_stream.prototype.stop)
- description and source-code
```javascript
stop = function () {
  this.emit('stopping');
  this.listening = false;
  this.socket.close();
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
