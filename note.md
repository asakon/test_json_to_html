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
