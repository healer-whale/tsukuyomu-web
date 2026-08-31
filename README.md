# tsukuyomu-web

短歌アプリ『つく×よむ』（iOS 配信中）の公式サイト。

公開先: https://healer-whale.github.io/tsukuyomu-web/

## ページ構成

| ファイル | 内容 |
| --- | --- |
| `index.html` | アプリ紹介（とは / 遊び方 / 特徴 / 画面 / ダウンロード / 最新のお知らせ） |
| `news.html` | お知らせ（不具合・アップデート・メンテナンス情報） |
| `privacy.html` | プライバシーポリシー |
| `style.css` | 全ページ共通スタイル |
| `assets/` | アイコン・ロゴ・favicon |
| `404.html` / `robots.txt` / `sitemap.xml` | 補助ファイル |
| `google8f9393ac4b241c10.html` | Google Search Console 認証ファイル（削除しない） |

ビルドツールは使っていません。ファイルをそのまま GitHub Pages で配信します。
パスはすべて相対パス（プロジェクトページ配信のため）。

## ローカル確認

```bash
python3 -m http.server 8000
# http://localhost:8000/ を開く
```

## お知らせの追加

`news.html` の先頭の `<article class="news-item">` ブロックをコピーして
`news-list` のいちばん上に貼り付け、日付・カテゴリ・本文を書き換える。
トップページにも最新分を載せる場合は `index.html` の「お知らせ」セクションにも同様に追記する。

カテゴリ（badge）:

- `<span class="badge">お知らせ</span>`
- `<span class="badge badge--update">アップデート</span>`
- `<span class="badge badge--bug">不具合</span>`
- `<span class="badge badge--maintenance">メンテナンス</span>`

## 素材の差し替え

- スクリーンショット: `index.html` の `.shot` プレースホルダーを `<img>` に置き換える
- アイコン・ロゴ: `assets/` 内。元データは別リポジトリ `TsukuYomu/assets/images/`
