# fukui-movie-fes

福井映画祭（Fukui Movie Festival）の映画情報を表示するシンプルな静的Webサイトです。コンテンツは単一のCSVファイルからブラウザ上で動的にレンダリングされます。

## ライブデモ

**[https://code4fukui.github.io/fukui-movie-fes/](https://code4fukui.github.io/fukui-movie-fes/)**

メインページでは、黒背景に映画ポスターがグリッド表示されます。別のページでは、検索可能な表形式で映画データの完全なリストを提供しています。

## 機能

-   **ポスターのグリッド表示:** CSVファイルから取得した映画のポスターとタイトルを、すっきりと見やすいレスポンシブなグリッドで表示します。
-   **表形式のデータ表示:** 専用ページ（`list.html`）にて、すべての映画データを検索・並べ替え可能な表形式で表示します。
-   **データ駆動:** すべてのコンテンツはクライアントサイドで `fukui-movie-fes_2024.csv` から読み込まれるため、更新が簡単です。
-   **ビルド不要:** Vanilla JavaScriptとWeb Componentsで構築されており、インストールやビルドプロセスは一切不要です。

## 仕組み

-   メインページ（`index.html`）では、[CSV.js](https://js.sabae.cc/CSV.js) ライブラリを使用して映画データを取得・解析し、ポスターのグリッドを動的に生成します。
-   リストページ（`list.html`）では、[code4fukui/csv-viewer](https://github.com/code4fukui/csv-viewer) の `<csv-viewer>` Webコンポーネントを使用して、CSVデータをインタラクティブな表としてレンダリングします。
-   サイト全体が静的であり、GitHub Pages上でホストされています。

## データソース

映画情報は `fukui-movie-fes_2024.csv` ファイルから取得され、以下の列が含まれています:
-   `id`: 一意の識別子
-   `title`: 映画のタイトル
-   `image`: 対応する画像ファイル名（例: `m1.jpg`）

## ローカルでの実行

1.  このリポジトリをクローンします。
2.  ローカルのWebサーバー（例: VS CodeのLive Server拡張機能や `python -m http.server`）を使用して、プロジェクトディレクトリをホストします。
3.  Webブラウザで、提供されたローカルURLを開きます。

*注: CSVファイルを取得する際のCORSエラーを回避するため、Webサーバーが必要です。*

## ライセンス

MIT License — 詳細は [LICENSE](LICENSE) を参照してください。
