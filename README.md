# Multiple Projects Proxy

このプロジェクトは、複数のVercelプロジェクトを同一ドメインで管理するためのプロキシプロジェクトです。

## 設定

`vercel.json`で以下のように設定されています：

- `/lp/` → `https://lp-project.vercel.app/`
- `/lp/*` → `https://lp-project.vercel.app/*`
- `/` → `https://main-site.vercel.app/`
- `/*` → `https://main-site.vercel.app/*`

## デプロイ手順

1. Vercelアカウントにログイン
2. このリポジトリをVercelにデプロイ
3. カスタムドメインを設定
4. `main-site.vercel.app`と`lp-project.vercel.app`を実際のプロジェクトURLに変更

## 確認方法

- `https://yourdomain.com/` → メインサイト
- `https://yourdomain.com/lp/` → LPサイト

## 注意点

- 外部URLへのrewritesが正常に動作するかテストが必要
- プランによる制限があるかもしれません