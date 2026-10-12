# サイト構成

静的HTML・CSS。外部ライブラリ、npm、ビルド処理への依存なし。

- index.html: 大会情報とルール導線
- pages/rules.html: ルール一覧
- pages/*.html: 分野別ルール
- css/tokens.css: 配色と幅
- css/base.css: 文字・基本要素
- css/components.css: 共通UI
- css/pages.css: ページレイアウト

すべて相対リンク。JavaScriptなしでも本文・ナビゲーションを読める。
現段階ではデータを表示する動的機能がないためJSファイルを作らない。
確定ルールと必要機能に応じてデータ管理・MAP表示・キラー検索を追加する。
共通ヘッダー・ナビゲーション・フッターは各HTMLに記載。変更時は全ページの整合を確認する。
