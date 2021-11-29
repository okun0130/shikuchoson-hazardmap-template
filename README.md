# 市区町村ハザードマップテンプレート

市区町村の Web ハザードマップを作成するためのテンプレート。\
[Tokyo OSS Party!!](https://tokyo-oss-party.com/) 2021 の成果物です。

テンプレート使用例: https://sankichi.net/shikuchoson-hazardmap-template/

## 背景と課題

国土交通省の管理する[ハザードマップポータルサイト](https://disaportal.gsi.go.jp/)では、以下の2つのサービスが提供されています。

- 重ねるハザードマップ: 災害リスク情報や防災に役立つ情報を、全国どこでも重ねて閲覧できるWeb地図サイト
- わがまちハザードマップ: 市町村が作成したハザードマップを見つけやすくまとめたリンク集

「重ねるハザードマップ」は多機能で非常によく作りこまれていますが、[使い方](https://disaportal.gsi.go.jp/hazardmap/pamphlet/pamphlet.html)でも

> 詳細を確認する場合は市町村が作成したハザードマップをご覧ください。

とあるとおり、あくまで国の作成した地図であり、市区町村ごとの詳細は確認できません。
自身の住む地域の詳細を確認するには、「わがまちハザードマップ」から市区町村のハザードマップを見る必要があります。
しかし、市区町村の作成するハザードマップの多くが紙での配布を前提としており、Webに最適化されていません。

このプロジェクトは、市区町村が Web ハザードマップを容易に作成・カスタマイズするためのテンプレートを提供します。

## 使い方

## 開発について

このプロジェクトは [Create React App](https://github.com/facebook/create-react-app) で作成されています。

以下のコマンドが使用可能です。

### `npm start`

開発モードでアプリを起動します。\
ブラウザで見るには [http://localhost:3000](http://localhost:3000) を開いてください。

コードを変更するたび、ページも更新されます。\
また、コンソールで lint エラーも確認できます。

### `npm run build`

本番向けのアプリをビルドし、`build` フォルダに配置します。

### `npm run prebuild`

`hazardmap-config.jsonc` や `csv` ディレクトリの内容をもとに、`src/generated` 以下のファイルを更新します。\
当該ファイル、ディレクトリに変更の変更を反映するには、`npm start` の前に一度このコマンドを実行してください。

### `npm run format`

`src` 以下のコードを整形します。\
フォーマッタには [Prettier](https://prettier.io/) を使用しています。
