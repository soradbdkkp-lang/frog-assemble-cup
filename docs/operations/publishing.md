# 公開手順

2026-10-29更新。

- リポジトリ：https://github.com/soradbdkkp-lang/frog-assemble-cup
- 公開サイト：https://soradbdkkp-lang.github.io/frog-assemble-cup/index.html
- 既存ブランチ：master。静的HTML・CSSで、インストールとビルドは不要。
- 公開対象：index.html、pages/、css/、assets/、.nojekyll。
- README・docsも公開リポジトリに含まれるため、秘匿情報を記録しない。

## 更新時の確認

1. 公開全8ページとリポジトリを照合し、最新のユーザー決定との差分を整理。
2. 関連ページと公開用文書を整合させる。変更指定のない規定は維持。
3. 全ページの内部リンク・アンカー・画像・メタ情報、スマホ表示を確認。
4. 対戦順・チーム表記・順位計算・応募表示を確認。公開ファイルと差分を秘匿情報・古い案内について検索。
5. git diff --checkを実行し、対象ファイルだけcommit。通常pushでmasterに反映し、既存のGitHub Pages配信を利用。履歴の強制上書きや配信設定変更は行わない。
6. 公開全8ページと参照CSS・画像のHTTP応答、更新後ソースとの一致と表示を確認。

今回のユーザー依頼は検証後のcommit・公開反映まで含む。応募フォームの実装・設定は別システムで、今回変更しない。
