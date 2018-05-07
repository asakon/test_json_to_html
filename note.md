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