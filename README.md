# 柏と3分 v0.1

真史さんのiPhoneで、柏さんと一緒に「国語・数学・英語を毎日少しだけ」続けるための超小型PWAです。

## 入っている機能
- 国語・数学・英語をタップで記録
- 1教科でも取り組めば、その日は記録あり
- 連続日数表示
- 最近7日の表示
- JSONバックアップ
- CSV書き出し（Excelで開きやすいUTF-8 BOM付き）
- JSONから復元
- オフライン利用
- 記録はiPhoneのブラウザ内に保存

## pCloudへのバックアップ
1. 「バックアップ（JSON）」をタップ
2. iPhoneの共有画面で「ファイルに保存」
3. 保存先として pCloud を選択
4. `kashiwa-3min-backup-YYYY-MM-DD.json` が保存されます

CSVも同じ方法です。

## iPhoneでPWAとして使う
PWAとしてインストールするには、HTTPSで公開する必要があります。
GitHub Pages / Cloudflare Pages / Netlify / Vercel などの静的ホスティングで十分です。
自前サーバーやデータベースは不要です。

公開後、iPhoneでURLを開き「ホーム画面に追加」します。
Braveでうまく表示されない場合は、インストール時だけSafariで同じURLを開いて追加してください。

## データについて
記録は `localStorage` に保存されます。
Safari/Braveのサイトデータ削除や端末トラブルに備え、定期的にJSONバックアップをpCloudへ保存してください。

## ファイル
- index.html
- manifest.json
- service-worker.js
- icon-192.png
- icon-512.png
