# npmtest-react-desktop

#### test coverage for  [react-desktop (v0.3.0)](https://github.com/gabrielbull/react-desktop#readme)  [![npm package](https://img.shields.io/npm/v/npmtest-react-desktop.svg?style=flat-square)](https://www.npmjs.org/package/npmtest-react-desktop) [![travis-ci.org build-status](https://api.travis-ci.org/npmtest/node-npmtest-react-desktop.svg)](https://travis-ci.org/npmtest/node-npmtest-react-desktop)

#### React UI Components for macOS Sierra and Windows 10

[![NPM](https://nodei.co/npm/react-desktop.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/react-desktop)

| git-branch : | [alpha](https://github.com/npmtest/node-npmtest-react-desktop/tree/alpha)|
|--:|:--|
| coverage : | [![istanbul-coverage](https://npmtest.github.io/node-npmtest-react-desktop/build/coverage.badge.svg)](https://npmtest.github.io/node-npmtest-react-desktop/build/coverage.html/index.html)|
| test-report : | [![test-report](https://npmtest.github.io/node-npmtest-react-desktop/build/test-report.badge.svg)](https://npmtest.github.io/node-npmtest-react-desktop/build/test-report.html)|
| build-artifacts : | [![build-artifacts](https://npmtest.github.io/node-npmtest-react-desktop/glyphicons_144_folder_open.png)](https://github.com/npmtest/node-npmtest-react-desktop/tree/gh-pages/build)|

- [https://npmtest.github.io/node-npmtest-react-desktop/build/coverage.html/index.html](https://npmtest.github.io/node-npmtest-react-desktop/build/coverage.html/index.html)

[![istanbul-coverage](https://npmtest.github.io/node-npmtest-react-desktop/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fcoverage.lib.html.png)](https://npmtest.github.io/node-npmtest-react-desktop/build/coverage.html/index.html)

- [https://npmtest.github.io/node-npmtest-react-desktop/build/test-report.html](https://npmtest.github.io/node-npmtest-react-desktop/build/test-report.html)

[![test-report](https://npmtest.github.io/node-npmtest-react-desktop/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Ftest-report.html.png)](https://npmtest.github.io/node-npmtest-react-desktop/build/test-report.html)

- [https://npmdoc.github.io/node-npmdoc-react-desktop/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-react-desktop/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-react-desktop/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-react-desktop/build/apidoc.html)

![npmPackageListing](https://npmtest.github.io/node-npmtest-react-desktop/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmtest.github.io/node-npmtest-react-desktop/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Gabriel Bull"
    },
    "bugs": {
        "url": "https://github.com/gabrielbull/react-desktop/issues"
    },
    "dependencies": {
        "radium": "^0.18.2"
    },
    "description": "React UI Components for macOS Sierra and Windows 10",
    "devDependencies": {
        "babel-cli": "^6.24.1",
        "babel-core": "^6.24.1",
        "babel-eslint": "^7.2.2",
        "babel-loader": "^6.4.1",
        "babel-plugin-transform-decorators-legacy": "^1.3.4",
        "babel-preset-es2015": "^6.24.1",
        "babel-preset-react": "^6.24.1",
        "babel-preset-stage-0": "^6.24.1",
        "chai": "^3.5.0",
        "eslint": "^3.19.0",
        "eslint-plugin-import": "^2.2.0",
        "eslint-plugin-react": "^6.10.3",
        "html-webpack-plugin": "^2.28.0",
        "jsdom": "^9.12.0",
        "mocha": "^3.2.0",
        "prop-types": "^15.5.8",
        "react": "^15.5.4",
        "react-addons-test-utils": "^15.5.1",
        "react-color": "^2.11.4",
        "react-dom": "^15.5.4",
        "react-hot-loader": "^1.3.1",
        "webpack": "^2.4.1",
        "webpack-dev-server": "^2.4.2"
    },
    "directories": {},
    "dist": {
        "shasum": "d5720b43f835b4c4ffc24864bb4f4ab79a2f2201",
        "tarball": "https://registry.npmjs.org/react-desktop/-/react-desktop-0.3.0.tgz"
    },
    "homepage": "https://github.com/gabrielbull/react-desktop#readme",
    "keywords": [
        "react",
        "react-component",
        "electron",
        "node-webkit",
        "native",
        "desktop",
        "ui",
        "user",
        "interface",
        "component",
        "os x",
        "macOS",
        "mac",
        "windows"
    ],
    "license": "MIT",
    "main": "./index.js",
    "maintainers": [
        {
            "name": "gabrielbull"
        }
    ],
    "name": "react-desktop",
    "optionalDependencies": {},
    "peerDependencies": {
        "prop-types": "^15.0 || ^16.0",
        "react": "^15.0 || ^16.0",
        "react-dom": "^15.0 || ^16.0"
    },
    "repository": {
        "type": "git",
        "url": "git+https://github.com/gabrielbull/react-desktop.git"
    },
    "scripts": {
        "build": "babel ./build/src --out-dir ./build/src && ./node_modules/.bin/babel ./build/index.js --out-file ./build/index.js && ./node_modules/.bin/babel ./build/macOs.js --out-file ./build/osx.js && ./node_modules/.bin/babel ./build/macOs.js --out-file ./build/macOs.js && ./node_modules/.bin/babel ./build/windows.js --out-file ./build/windows.js",
        "build-publish": "npm run build && npm publish ./build",
        "eslint": "eslint ./src ./test",
        "playground": "webpack-dev-server --config ./playground/webpack.config.js --colors --inline --port 3001",
        "prebuild": "rsync -av -delete . build --exclude build --exclude .git --exclude .idea && npm run eslint && npm run test",
        "test": "mocha test"
    },
    "version": "0.3.0"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
