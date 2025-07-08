# デプロイ手順

## 1. GitHubリポジトリを手動で作成

### main-site-test用
1. GitHub.comにログイン
2. 新しいリポジトリを作成: `main-site-test`
3. 以下のコマンドを実行:

```bash
cd test-projects/main-site-test
git remote add origin https://github.com/YOUR_USERNAME/main-site-test.git
git branch -M main
git push -u origin main
```

### lp-project-test用
1. GitHub.comにログイン
2. 新しいリポジトリを作成: `lp-project-test`
3. 以下のコマンドを実行:

```bash
cd ../lp-project-test
git init
git add .
git commit -m "Initial commit"
git remote add origin https://github.com/YOUR_USERNAME/lp-project-test.git
git branch -M main
git push -u origin main
```

## 2. Vercelにデプロイ

1. Vercel.comにログイン
2. 「New Project」をクリック
3. 作成したGitHubリポジトリを選択してデプロイ
4. 両方のプロジェクトをデプロイ

## 3. 実際のURLを取得

デプロイ後、以下のような形式のURLが生成されます:
- `https://main-site-test.vercel.app/`
- `https://lp-project-test.vercel.app/`

## 4. プロキシプロジェクトの設定更新

取得したURLでvercel.jsonを更新してください。