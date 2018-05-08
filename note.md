# note

## GAS
- 参考：Google SpreadSheet のデータを JSON 形式で取得する Web API をサクッと作る - Qiita 
  - https://qiita.com/takatama/items/7aa1097aac453fff1d53
- 関数を指定してデバッグ実行してもJSONは得られなかった。なぜ？
- とりあえずAPI、ということで
- 実行可能APIはステップがいろいろ…
  - https://qiita.com/soundTricker/items/1bcfc5c9e80d29a7ae4b

### APIのURLの確認方法
  - 公開 > ウェブアプリケーションとして導入... > 現在のウェブ アプリケーションの URL:

## EJSではなくpugにした 
- シンプルな記法のpugに挑戦

## 環境作る
```
npm -v
gulp -v
npm init
npm install gulp --save-dev
```
- 参考：https://tnyk.jp/frontend/269/
```
npm install -D gulp-data jsonfile
```
### リモートリポジトリ急いで作る
- GitHubに急いで作ってSSHのを（）コピー
- git remote add origin ホニャ
- なんとなくmasterをチェックアウトしないとまずそうな流れを感じる
- git push -u origin master
- 元のブランチをチェックアウトしてpush

## 作業再開
- gulpfile
  - require
  - 結局ぜんぶrequire
  - browserSync OK

## pugやってみよう
- https://pugjs.org/api/getting-started.html
- npm install pug
```
$ npm install pug
| |-----------------------------------------------------------------------------------------
test_json_to_html@1.0.0 D:\work\src\test_json_to_html
`-- pug@2.0.3  extraneous

npm WARN optional Skipping failed optional dependency /chokidar/fsevents:
npm WARN notsup Not compatible with your operating system or architecture: fsevents@1.2.3
```
- 大丈夫か？(extraneous: 無関係の、外来の)
- pug -v が無反応...入ってない

### pugのgithubのreadmeを見る
- https://github.com/pugjs/pug
- npm install -D pug-cli を試す
- 「-g使え」と怒られるものの、入った
```
$ npm install -D  pug-cli
npm WARN prefer global pug-cli@1.0.0-alpha6 should be installed with -g
test_json_to_html@1.0.0 D:\work\src\test_json_to_html
+-- pug@2.0.3
`-- pug-cli@1.0.0-alpha6

npm WARN optional Skipping failed optional dependency /chokidar/fsevents:
npm WARN notsup Not compatible with your operating system or architecture: fsevents@1.2.3
```
- pug -v も pug-cli -v も反応なし
- package.jsonに "pug-cli": "^1.0.0-alpha6" が入っている
- pug --help に反応がない…
- 不安になったので、とりあえず、npm install pug > 同じバージョンが入った。pug --helpは反応が無い...
- さらにpug-cliも-gでインストールを試す。今度はnodistに入ったログが出た。pug --helpに反応があった！
```
$ npm install pug-cli -g
d:\Program Files (x86)\Nodist\bin\pug -> d:\Program Files (x86)\Nodist\bin\node_modules\pug-cli\index.
js
d:\Program Files (x86)\Nodist\bin
`-- pug-cli@1.0.0-alpha6
  +-- chalk@1.1.3
  | +-- ansi-styles@2.2.1
  | +-- escape-string-regexp@1.0.5
  | +-- has-ansi@2.0.0
  | | `-- ansi-regex@2.1.1
  | +-- strip-ansi@3.0.1
  | `-- supports-color@2.0.0
  +-- commander@2.15.1
  +-- mkdirp@0.5.1
  | `-- minimist@0.0.8
  `-- pug@2.0.3
    +-- pug-code-gen@2.0.1
    | +-- constantinople@3.1.2
    | | +-- @types/babel-types@7.0.1
    | | +-- @types/babylon@6.16.2
    | | +-- babel-types@6.26.0
    | | | +-- babel-runtime@6.26.0
    | | | | +-- core-js@2.5.6
    | | | | `-- regenerator-runtime@0.11.1
    | | | +-- esutils@2.0.2
    | | | +-- lodash@4.17.10
    | | | `-- to-fast-properties@1.0.3
    | | `-- babylon@6.18.0
    | +-- doctypes@1.1.0
    | +-- js-stringify@1.0.2
    | +-- pug-attrs@2.0.3
    | +-- pug-error@1.3.2
    | +-- void-elements@2.0.1
    | `-- with@5.1.1
    |   +-- acorn@3.3.0
    |   `-- acorn-globals@3.1.0
    |     `-- acorn@4.0.13
    +-- pug-filters@3.1.0
    | +-- clean-css@4.1.11
    | | `-- source-map@0.5.7
    | +-- jstransformer@1.0.0
    | | +-- is-promise@2.1.0
    | | `-- promise@7.3.1
    | |   `-- asap@2.0.6
    | +-- pug-walk@1.1.7
    | +-- resolve@1.7.1
    | | `-- path-parse@1.0.5
    | `-- uglify-js@2.8.29
    |   +-- uglify-to-browserify@1.0.2
    |   `-- yargs@3.10.0
    |     +-- camelcase@1.2.1
    |     +-- cliui@2.1.0
    |     | +-- center-align@0.1.3
    |     | | +-- align-text@0.1.4
    |     | | | +-- kind-of@3.2.2
    |     | | | | `-- is-buffer@1.1.6
    |     | | | +-- longest@1.0.1
    |     | | | `-- repeat-string@1.6.1
    |     | | `-- lazy-cache@1.0.4
    |     | +-- right-align@0.1.3
    |     | `-- wordwrap@0.0.2
    |     +-- decamelize@1.2.0
    |     `-- window-size@0.1.0
    +-- pug-lexer@4.0.0
    | +-- character-parser@2.2.0
    | | `-- is-regex@1.0.4
    | |   `-- has@1.0.1
    | |     `-- function-bind@1.1.1
    | `-- is-expression@3.0.0
    |   `-- acorn@4.0.13
    +-- pug-linker@3.0.5
    +-- pug-load@2.0.11
    | `-- object-assign@4.1.1
    +-- pug-parser@5.0.0
    | `-- token-stream@0.0.1
    +-- pug-runtime@2.0.4
    `-- pug-strip-comments@1.0.3


as@as02 MINGW64 /d/work/src/test_json_to_html (try_pug)
$
```
### gulpfileを書こうとしたがよく分からなくなったので参考サイト変更
- ゴリラ https://blog.mismithportfolio.com/web/20160326pugbegin
- index.pugを作ってpug index.pugしたらindex.htmlができた！
- onelineではなく整形したものもレンダされた！ pug index.pug --pretty
