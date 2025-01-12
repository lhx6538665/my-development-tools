<a name="top"></a>
# NodeJS 开发工具栈

[⬅︎ 返回上层](../#nodejs-开发)

## TOC

<!-- MarkdownTOC depth=2 GFM -->

- [Node 环境](#node-环境)
- [Misc](#misc)
- [通知](#通知)
- [事件/Event Emitter](#事件event-emitter)
- [随机数](#随机数)
- [CLI](#cli)
    - [自动补全](#自动补全)
    - [REPL / 交互式 CLI](#repl--交互式-cli)
    - [CLI 参数解析](#cli-参数解析)
    - [颜色 (Color)](#颜色-color)
- [颜色](#颜色)
- [脚本](#脚本)
- [打包方案](#打包方案)
- [工具集](#工具集)
- [debug](#debug)
- [数据校验](#数据校验)
- [脚手架](#脚手架)
- [测试](#测试)
- [Benchmark](#benchmark)
- [服务器](#服务器)
- [数据生成/Mock](#数据生成mock)
- [错误处理](#错误处理)
- [配置](#配置)
- [日志](#日志)
- [进程](#进程)
- [文件](#文件)
    - [模板](#模板)
- [网络](#网络)
- [文档](#文档)
- [时间](#时间)
- [单位换算](#单位换算)
- [工程化](#工程化)
- [自动化](#自动化)
- [ORM](#orm)
- [AST](#ast)
- [Code Lint](#code-lint)
- [Profiling](#profiling)
- [HTTP](#http)
- [安全](#安全)
- [Node 客户端](#node-客户端)
- [框架](#框架)
- [Stream](#stream)
- [压缩/解压](#压缩解压)
- [语法分析](#语法分析)
- [evil](#evil)
- [SSL](#ssl)
- [NPM](#npm)
- [序列化](#序列化)
- [其他](#其他)
- [我关注的人/组](#我关注的人组)
- [待评价](#待评价)

<!-- /MarkdownTOC -->

## Node 环境

- [nrm](https://github.com/Pana/nrm): NPM Registry Manager
- [nvm](https://github.com/creationix/nvm): Node Version Manager
- [nvs](https://github.com/jasongin/nvs): 与 nvm 类似。只是因为 nvm 对 windows 的支持跟 linux 不一样。用 nvs 命令调用统一。

## Misc

- [dependency-check](https://github.com/maxogden/dependency-check): 依赖检查，确保引用的模块已写在 package.json
- [yn](https://github.com/sindresorhus/yn): 判断值是否为 yes/no
- [package-json](https://github.com/sindresorhus/package-json): Get metadata of a package from the npm registry. 支持私有 registry

## 通知

- [node-notifier](https://github.com/mikaelbr/node-notifier): 调用系统通知 API，兼容很多系统

## 事件/Event Emitter

- [tiny-emitter](https://github.com/scottcorgan/tiny-emitter)

## 随机数

- [nano-id-cc](https://zelark.github.io/nano-id-cc/): 碰撞计算器
- [shortid](https://github.com/dylang/shortid)
- [nanoid](https://github.com/ai/nanoid)

## CLI

- [cli-cheatsheet](https://github.com/sw-yx/cli-cheatsheet): 一份手册。收集了很多很棒的类库
- [blessed](https://github.com/chjj/blessed): 强大的 CLI UI 开发工具集
  - [blessed-contrib](https://github.com/yaronn/blessed-contrib): blessed 扩展
- [wopr](https://github.com/yaronn/wopr): CLI 图形化报表
- [iponmap](https://github.com/nogizhopaboroda/iponmap): IP 地图映射
- [babar](https://github.com/stephan83/babar): CLI Chart
- [clui](https://github.com/nathanpeck/clui): Command Line UI toolkit
- [cli-spinners](https://github.com/sindresorhus/cli-spinners): 终端里的 Spinner
- [ora](https://github.com/sindresorhus/ora): 同 cli-spinners
- [cli-table2](https://github.com/jamestalmage/cli-table2): 表格输出
- [cliff](https://github.com/flatiron/cliff): 格式化输出
- [update-notifier](https://github.com/yeoman/update-notifier): 「非常不好用，寻找替代品」命令行版本更新提醒
- [shelljs](https://github.com/shelljs/shelljs): unix 命令的 nodejs 封装
- [node-draftlog](https://github.com/ivanseidel/node-draftlog): 单行动态变化的终端打印
- [gauge](https://github.com/iarna/gauge): 进度条
- [node-progress](https://github.com/visionmedia/node-progress): 进度条
- [prettyjson](https://github.com/rafeca/prettyjson): 把 JSON 数据按 YAML 风格打印出来

### 自动补全

- [tabtab](https://github.com/mklabs/tabtab): 命令行自动补全

### REPL / 交互式 CLI

- [Mancy](https://github.com/princejwesley/Mancy): Electron based NodeJS REPL
- [nesh](https://github.com/danielgtaylor/nesh): 增强型交互式 shell 框架
- [vorpal](https://github.com/dthree/vorpal): 交互式命令行框架
- [vantage](https://github.com/dthree/vantage): 实时交互式 CLI 工具，基于 vorpal 开发
- [runkit](https://runkit.com/home): 非常酷！在前端直接引用 npm 包编写代码
- [ink](https://github.com/vadimdemedes/ink): 用 React 写法构建交互式 CLI
  - [ink-tab](https://github.com/jdeniau/ink-tab)

### CLI 参数解析

- [yargs](https://github.com/yargs/yargs): 命令行参数解析器（复杂版）。支持子命令，多语言，帮助文档等功能
- [minimist](https://github.com/substack/minimist): 命令行参数解析器（极简）
- [Inquirer](https://github.com/SBoudrias/Inquirer.js): 命令行交互提示
  - [Enquirer](https://github.com/enquirer/enquirer): 类似 Inquirer，UI 交互更丰富
  - [qoa](https://github.com/klaussinani/qoa): 备选方案
- [Caporal.js](https://github.com/mattallty/Caporal.js): 支持自动补全，自动构建帮助，语法友好的 CLI 框架。缺点是不支持 global option，详见 [issue](https://github.com/mattallty/Caporal.js/issues/21)
  - [oclif](https://github.com/oclif/oclif): Heroku 出品。功能跟 Caporal.js 类似。特点是 OOP，Hook，插件更胜一筹
    - [12 Factor CLI App](https://medium.com/@jdxcode/12-factor-cli-apps-dd3c227a0e46)
  - [commander.js](https://github.com/tj/commander.js): 比 Caporal 弱一点。备选方案

### 颜色 (Color)

- [cli-color](https://github.com/medikoo/cli-color): 终端颜色
  - [colorette](https://github.com/jorgebucaran/colorette): 备选方案，速度最快
  - [chalk](https://github.com/chalk/chalk): 终端颜色。同 cli-color，备选方案，速度最慢
- [strip-ansi](https://github.com/chalk/strip-ansi): 虽然 cli-color 也有 [strip](https://github.com/medikoo/cli-color#clcstripformatedtext)，这个 library 只做一件事，依赖模块较少
- [gradient-string](https://github.com/bokub/gradient-string): 过渡色
- [chalk-animation](https://github.com/bokub/chalk-animation): 终端颜色动画

## 颜色

- [chromatism](https://github.com/toish/chromatism): 颜色转换

## 脚本

- [npm-run-all](https://github.com/mysticatea/npm-run-all): 用于 npm scripts，并行/顺序执行多个子 script
- [husky](https://github.com/typicode/husky): git hook
- [lint-staged](https://github.com/okonet/lint-staged): Run commands on git staged files

## 打包方案

- [pkg](https://github.com/zeit/pkg): 将 node 脚本编译成可执行二进制文件，脱离 node 依赖
- [enclose](https://github.com/igorklopov/enclose):  pkg 的前身，都是由 igorklopov 开发的，记录以作纪念
- [nexe](https://github.com/nexe/nexe): 另一套打包成可执行程序的方案
- [node-packer](https://github.com/pmq20/node-packer): 又一套打包成可执行程序的方案

方案比较
- https://github.com/zeit/pkg/issues/42
- https://github.com/pmq20/node-packer#comparing-with-similar-projects

## 工具集

- [debug](https://github.com/visionmedia/debug): debug 工具
- [power-assert](https://github.com/power-assert-js/power-assert): 非常强大的 assert 工具，兼容生产环境
- [LoDash](https://github.com/lodash/lodash): 日常开发工具集
- [Ramda](https://github.com/ramda/ramda): 函数式编程工具集
- [bluebird](https://github.com/petkaantonov/bluebird): 强大的 Promise 库
  - [promise-fun](https://github.com/sindresorhus/promise-fun): 轮子王造的独立的函数库
  - [aigle](https://github.com/suguru03/aigle): bluebird 替代方案
- [co](https://github.com/tj/co): 强大的异步处理库
- [utility-maker](https://github.com/adoyle-h/utility-maker): 定义自己的工具集
- [is](https://github.com/arasatasaygin/is.js): 类型判断
- [json-parse-helpfulerror](https://github.com/smikes/json-parse-helpfulerror): json 解析错误时，给出人类友好的提示
- [string-template](https://github.com/Matt-Esch/string-template): 字符串变量拼接
- [updeep](https://github.com/substantial/updeep): 修改深层嵌套的 object 或 array
- [immer](https://github.com/mweststrate/immer): 比较优雅的 Immutable.js alternative。基于 Proxy 的特性
  - [immutable-js](https://github.com/facebook/immutable-js/): Immutable.js
- [safe-touch](https://github.com/EnixCoda/safe-touch): 类似 lodash.get 但书写更友好，[介绍](https://zhuanlan.zhihu.com/p/39751773)
- [prettier-package-json](https://github.com/cameronhunter/prettier-package-json): 格式化 package.json

## debug

- [Node.js 调试指南](https://github.com/nswbmw/node-in-debugging): 必读
- [JavaScript Debugging Reference](https://developers.google.com/web/tools/chrome-devtools/javascript/reference): Chrome DevTools 的 Debug 功能
- [ndb](https://github.com/GoogleChromeLabs/ndb): 基于 Chrome DevTools 的增强 Debug 功能
- [node-clinic](https://github.com/nearform/node-clinic)

## 数据校验

- [Joi](https://github.com/hapijs/joi): 人类友好的校验 Schema
- [yup](https://github.com/jquense/yup): 同 Joi，备用

## 脚手架

- [yo](https://github.com/yeoman/yo): 脚手架工具

## 测试

- [jest](https://github.com/facebook/jest): 测试框架，前后端通用，支持 ts、babel 等扩展。
    - [ava](https://github.com/avajs/ava): 备选方案
- [nyc](https://github.com/istanbuljs/nyc): 测试覆盖率
- [sinon](https://github.com/sinonjs/sinon): Stub/Mock/Spie 工具库
- [supertest](https://github.com/visionmedia/supertest): 测试 http 服务器
- [rewire](https://github.com/jhnns/rewire): 改写模块内未暴露的变量

## Benchmark

- [benchmark.js](https://github.com/bestiejs/benchmark.js): Benchmark 框架
- [beautify-benchmark](https://github.com/Fishrock123/beautify-benchmark): 格式化 benchmark.js 的输出
- [Chūhai](https://github.com/Hypercubed/chuhai): 测试驱动的 Benchmark
- [matcha](https://github.com/logicalparadox/matcha): mocha 类似语法的，输出友好的 Benchmark 框架

## 服务器

- [json-server](https://github.com/typicode/json-server): 快速搭建 HTTP RESTFul API Server
- [http-server](https://github.com/indexzero/http-server): 快速搭建 HTTP 服务器，主要用于提供静态文件访问
  - [serve](https://github.com/zeit/serve): alternative
- [lowdb](https://github.com/typicode/lowdb): 本地 json 数据库
- [micro](https://github.com/zeit/micro): 零配置的 HTTP 服务器，非常轻量好用，主要用于实现简单的逻辑
- [stoppable](https://github.com/hunterloftis/stoppable): graceful shutdown
- [terminus](https://github.com/godaddy/terminus): 封装了 stoppable 和进程信号处理，增加了一些进程退出前的自定义回调和 k8s 健康检查的回调。

## 数据生成/Mock

- [faker.js](https://github.com/Marak/faker.js): 制造假数据
- [casual](https://github.com/boo1ean/casual): 制造假数据。备选
- [Chance](https://github.com/chancejs/chancejs): 制造假数据。备选2
- [nuysoft/Mock](https://github.com/nuysoft/Mock): 制造假数据。备选3
- [json-schema-faker](https://github.com/json-schema-faker/json-schema-faker): 根据 json schema 生成数据
- [nock](https://github.com/nock/nock): HTTP server mocking and expectations library for Node.js

## 错误处理

- [ero.js](https://github.com/adoyle-h/Ero.js): 自定义 Error 类
- [pretty-error](https://github.com/AriaMinaei/pretty-error): 打印人类友好的错误堆栈
- [koajs/onerror](https://github.com/koajs/onerror): 响应错误页面
- [node-retry](https://github.com/tim-kos/node-retry): 重试
- [longjohn](https://github.com/mattinsler/longjohn): 跟踪完整的调用堆栈

## 配置

- [node-config](https://github.com/lorenwest/node-config): 多环境应用层配置
- [dotenv](https://github.com/motdotla/dotenv): 读取 `.env` 文件设置环境变量。
  - 首先要了解它的[使用场景](https://github.com/motdotla/dotenv#faq)
- [cosmiconfig](https://github.com/davidtheclark/cosmiconfig): Find and load configuration from a package.json property, rc file, or CommonJS module

## 日志

- [signale](https://github.com/klaussinani/signale): 高度可扩展的 log 库
- ~~[winston](https://github.com/winstonjs/winston)~~: 备选方案。修复 Issue 太慢，在高并发下可能存在严重的性能问题。

## 进程

- [nodemon](https://github.com/remy/nodemon): 守护进程。本地开发用，文件改动时自动重启 node 应用
- [PM2](https://github.com/Unitech/pm2): 进程管理。生产环境用
- [pandora](https://github.com/midwayjs/pandora/): Node.js 应用监控管理器，自带 Metrics，请求链路跟踪，可扩展。

## 文件

- [npm/ini](https://github.com/npm/ini): `ini` 文件解析器
- [node-properties-parser](https://github.com/xavi-/node-properties-parser): `.properties` 文件解析器
- [js-yaml](https://github.com/nodeca/js-yaml): `YAML` 文件解析器
- [glob](https://github.com/isaacs/node-glob): 文件匹配搜索
  - [fast-glob](https://github.com/mrmlnc/fast-glob): alternative
- [vinyl](https://github.com/gulpjs/vinyl): 用 JS 描述文件
- [chokidar](https://github.com/paulmillr/chokidar): 监听文件变化
- [jschardet](https://github.com/aadsm/jschardet): Character encoding auto-detection in JavaScript (port of python's chardet)

### 模板

- [assemble](https://github.com/assemble/assemble): 模板文件搭建工具
- [consolidate](https://github.com/tj/consolidate.js): 模板引擎抽象层
- [templates](https://github.com/jonschlinkert/templates): 模板引擎抽象层

## 网络

- [address](https://github.com/node-modules/address): 获取本机的网络地址(ipv4/ipv6/mac/dns)
- [detect-port](https://github.com/node-modules/detect-port): 获取可用端口

## 文档

- [documentation.js](https://github.com/documentationjs/documentation): documentation for modern JavaScript. 基于 JSDoc 渲染文档，支持很多酷炫的特性，支持输出 HTML/Markdown/JSON
- [esdoc](https://github.com/esdoc/esdoc): JSDoc 当前不支持 ES6 语法，或许可以尝试使用这个
- [all-contributors](https://github.com/kentcdodds/all-contributors): 贡献统计
- [verb](https://github.com/verbose/verb): 文档生成器的生成器
- [mos](https://github.com/mosjs/mos): 自动生成 Markdown 内嵌代码片段。插件化

## 时间

- [moment](https://github.com/moment/moment): 最强大的时间库
- [moment-range](https://github.com/gf3/moment-range): 时间段内插值
- [date-fns](https://github.com/date-fns/date-fns): 类似 moment
- [ms](https://github.com/zeit/ms)
- [pretty-ms](https://github.com/sindresorhus/pretty-ms)
- [node-microtime](https://github.com/wadey/node-microtime)

## 单位换算

- [bytes](https://github.com/visionmedia/bytes.js): b/kb/mb/gb/tb 转换

## 工程化

- [node-rfr](https://github.com/warmsea/node-rfr): module.require 增强，避免使用相对路径
- [tapable](https://github.com/webpack/tapable): 实现插件机制
- [lerna](https://github.com/lerna/lerna): 在一个代码仓库中维护多个 package 的工具

## 自动化

- [gulp](https://github.com/gulpjs/gulp)
- [webpack](https://github.com/webpack/webpack)

## ORM

没有好用的 ORM

## AST

- [recast](https://github.com/benjamn/recast): JavaScript syntax tree transformer, nondestructive pretty-printer, and automatic source map generator
- [jscodeshift](https://github.com/facebook/jscodeshift): 改写 js 代码
- [js-codemod](https://github.com/cpojer/js-codemod): a collection of codemod scripts for use with JSCodeshift

## Code Lint

- [eslint](https://github.com/eslint/eslint): 规则式代码校验器
  - [eslint-plugin-import](https://github.com/benmosher/eslint-plugin-import)
  - [eslint-import-resolver-alias](https://github.com/johvin/eslint-import-resolver-alias)

## Profiling

- [source-map-explorer](https://github.com/danvk/source-map-explorer): 根据 sourcemap 分析代码占用空间
- [plato](https://github.com/es-analysis/plato): 代码复杂度分析工具

## HTTP

- [urijs](https://github.com/medialize/URI.js): uri 解析处理
- [axios](https://github.com/mzabriskie/axios): HTTP 请求客户端，参数配置化，API 设计简洁合理。
  - 但是 POST 请求处理有个缺点: https://github.com/mzabriskie/axios/issues/362
  - [ky](https://github.com/sindresorhus/ky): 前端备选方案
  - [got](https://github.com/sindresorhus/got): 后端备选方案
- [superagent](https://github.com/visionmedia/superagent): HTTP 请求客户端。特点是支持插件，缺点是文档写得不够好。

## 安全

- [nsp](https://github.com/nodesecurity/nsp): node 代码安全检查

## Node 客户端

- [ioredis](https://github.com/luin/ioredis): redis client

## 框架

- [koa](https://github.com/koajs/koa): http 框架
- [hapi](https://github.com/hapijs/hapi): http 框架。备选
- [meteor](https://github.com/meteor/meteor): 实时数据框架

## Stream

- [through2](https://github.com/rvagg/through2): Tiny wrapper around Node streams2 Transform to avoid explicit subclassing noise
- [concat-stream](https://github.com/maxogden/concat-stream): writable stream that concatenates strings or data and calls a callback with the result
- [multipipe](https://github.com/juliangruber/multipipe): A better `Stream.pipe` that creates duplex streams and lets you handle errors in one place.
- [node-streamifier](https://github.com/iSkore/node-streamifier): Converts a Buffer/String to a readable stream.

## 压缩/解压

- [compressing](https://github.com/node-modules/compressing): 支持 stream
  - [tar-stream](https://github.com/mafintosh/tar-stream): compressing 依赖 tar-stream

## 语法分析

- [esprima](https://github.com/jquery/esprima): ECMAScript parsing infrastructure for multipurpose analysis
- [babylon](https://github.com/babel/babylon): 同 esprima
- [acorn](https://github.com/ternjs/acorn): 同 esprima，性能或许更好
- [shift](https://github.com/shapesecurity/shift-parser-js): 同 esprima
- [astexplorer](https://astexplorer.net/): AST 浏览器
- [estools](https://github.com/estools): ECMAScript Tooling
  - [escodegen](https://github.com/estools/escodegen): 根据 AST 生成代码
- [pegjs](https://github.com/pegjs/pegjs): Parser generator for JavaScript

## evil

- [notevil](https://github.com/mmckegg/notevil): 结合 AST 的 evil
- [static-eval](https://github.com/substack/static-eval): 结合 AST 的 evil。需要自己传入 AST

## SSL

- [openssl-self-signed-certificate](https://github.com/neverendingqs/openssl-self-signed-certificate): 别人已做好的 SSL 证书，辅助快速开发

## NPM

- [verdaccio](https://github.com/verdaccio/verdaccio): NPM 私有仓库
  - [cnpmjs.org](https://github.com/cnpm/cnpmjs.org)
- [yarn](https://github.com/yarnpkg/yarn): 安装速度确实比 NPM 快很多
  - [yarn-completion](https://github.com/dsifford/yarn-completion): bash 自动补全
- [np](https://github.com/sindresorhus/np): A better `npm publish`

## 序列化

- [fast-json-stringify](https://github.com/fastify/fast-json-stringify): 比原生的 `JSON.stringify()` 快
- [serialize-javascript](https://github.com/yahoo/serialize-javascript): 序列化 JS，支持函数、正则表达式

## 其他

- [license-checker](https://github.com/davglass/license-checker): Check NPM package licenses
- [cz-cli](https://github.com/commitizen/cz-cli): 规范 git commit message
- [none](https://github.com/dak0rn/none): 空。在特殊场景可以用到
- [cheerio](https://github.com/cheeriojs/cheerio): 服务端运行的 jQuery
- [jsdiff](https://github.com/kpdecker/jsdiff): diff library
- [franc](https://github.com/wooorm/franc): 自然语言判断
- [node-temp](https://github.com/bruce/node-temp): 产生临时目录文件
- [jsdom](https://github.com/tmpvar/jsdom): 在 nodejs 使用符合 WHATWG 和 HTML 标准的 JS DOM
- [open](https://github.com/sindresorhus/open): 很方便的打开网站，文件，或可执行文件的命令
- [fast-deep-equal](https://github.com/epoberezkin/fast-deep-equal)

## 我关注的人/组

- https://github.com/sindresorhus?utf8=%E2%9C%93&tab=repositories&q=&type=source
- https://github.com/DJCordhose?utf8=%E2%9C%93&tab=repositories&q=&type=source
- https://github.com/substack?utf8=%E2%9C%93&tab=repositories&q=&type=source
- https://github.com/isaacs?utf8=%E2%9C%93&tab=repositories&q=&type=source

- https://github.com/node-modules

----

## 待评价


**[⬆ 返回顶部](#top)**
