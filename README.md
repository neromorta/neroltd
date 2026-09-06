# NERO MOTORING YARD Website

GitHub と Netlify で公開するための、ビルド不要な静的サイトです。`index.html` を直接配信します。

## ローカル確認

PowerShell でこのフォルダを開き、以下を実行します。

```powershell
py -m http.server 4173
```

その後、`http://localhost:4173` を開いてください。

## GitHub / Netlify への公開

1. GitHub で非公開または公開リポジトリを作成し、このフォルダの全ファイルを push します。
2. Netlify で GitHub を接続し、作成したリポジトリを選択します。
3. Build command は空欄、Publish directory は `.` のまま Deploy します。
4. Netlify の Domain management で `nero-ltd.co.jp` と `www.nero-ltd.co.jp` を追加します。
5. 現在の DNS 管理画面で、Netlify が表示する A / CNAME レコードへ切り替えます。メール用の MX、SPF、DKIM レコードは変更しないでください。

## 問い合わせフォーム

フォームは Netlify Forms を使用します。公開後、Netlify 管理画面の **Forms** に `contact` が自動登録されます。送信通知先メールアドレスは、公開後に Netlify の Forms notifications で設定してください。

## 既存 URL の扱い

`/services`、`/contact`、`/newcar` は `netlify.toml` により新しい該当セクションへ転送します。既存の検索結果やブックマークへの配慮です。
