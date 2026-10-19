# フェリスの自己紹介ページ

カオス理論（ローレンツ・アトラクタ）で動く自己紹介ページです。

公開URL: `https://ユーザー名.github.io/リポジトリ名/`

## ファイル
- `index.html` … トップページ
- `detail.html` … 詳細ページ（内容は中の `D = {...}` を編集）
- `.nojekyll` … GitHub Pagesにそのまま公開するための空ファイル

## 公開方法（コマンド1回）
GitHub CLI（`gh`）を使う場合、このフォルダで次を実行します。

```bash
git init -b main && git add . && git commit -m "init"
gh repo create felis-site --public --source=. --push
gh api -X POST repos/{owner}/felis-site/pages -f "source[branch]=main" -f "source[path]=/"
```

1〜2分後に `https://ユーザー名.github.io/felis-site/` で開けます。

## 公開方法（ブラウザだけ）
1. リポジトリにファイルをアップロードする
2. Settings → Pages → Branch を `main` / `(root)` にして Save
