# 公開前Git整理（2026-10-12）

## 管理対象の分類

- 必須：index.html、pages/ の7 HTML、css/ の4 CSS、assets/images/ の29 WebP、.nojekyll。
- 推奨：README.md、docs/ の要件・参照履歴・設計・運用文書、.gitattributes、.gitignore。
- 不要：frogcup-vol1.zip（素材元のローカル資料。必要画像は抽出済みでサイトから未参照）。削除せずルートの当該ファイルだけignoreする。
- favicon、JavaScript、外部フォント、ビルド用ファイルへの依存はない。

## 検証

ステージ済みGitファイルの内容だけを読み取るローカルHTTPサーバーで検証。作業ツリーの未管理ファイルやZIPは使用しない。

- HTML・CSS内のローカル参照216件：正確な大文字小文字のGitパスとリンク先IDがすべて存在。
- 全8 HTML、4 CSS、29画像を管理。参照先HTTP取得はすべて200。Markdownの相対リンクも存在確認済み。
- Edgeで全8ページを375px・390px・1280px表示。ページ全体の横はみ出し、壊れた画像なし。
- 全ページの「応募」ナビからトップの応募欄へ到達。トップの応募CTA2件と参加案内の応募リンクを確認。
- 正式応募フォームはHTTP 200。入力・応募送信は未実施。
- ブラウザーの自動取得 /favicon.ico は未設定のため404。HTMLから参照される欠落ではなく、favicon追加は今後の改善項目。
- git diff --check / git diff --cached --check：合格。既存文書の行末空白のみ除去。

## 公開工程への引き継ぎ

サイトをGit管理対象だけで再現可能。応募導線commit 49b18150a55bc2c569558124de9334a832c60ef1 は保持する。remote追加・リポジトリ作成・push・Pages設定・本番公開は今回行わない。
公開先を決め、index.html、pages/、css/、assets/、.nojekyll を配信し、運営用docsとREADMEを配信対象から除く方法を選ぶ。公開URLで最終確認する。
