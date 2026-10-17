# My Portfolio

このリポジトリは、Next.js（App Router）をベースに構築した個人ポートフォリオサイトのソースコードです。デザインやコンポーネント構成を通して、フロントエンドのスキルセットや実務での開発スタイルを確認できるように構成しています。

## 技術スタック

- **Framework:** Next.js (App Router)
- **Language:** TypeScript
- **Package Manager:** pnpm
- **Styling:** （ここに使用しているCSSフレームワークやツールがあれば記載）
- **Lint / Format:** ESLint, （Prettierなど使用していれば追記）
- **その他:** next/font（Geist）

必要に応じて、実際に使用しているライブラリやサービス（UIライブラリ、分析ツール、認証、CMS など）を追記してください。

## セットアップ

このプロジェクトをローカルで動かすには、Node.js と pnpm（または npm / yarn / bun）が必要です。

1. リポジトリをクローンします。

```bash
git clone <YOUR_REPOSITORY_URL>
cd my-portfolio
```

2. 依存関係をインストールします。

```bash
pnpm install
# または
npm install
# または
yarn install
# または
bun install
```

3. 開発サーバーを起動します。

```bash
pnpm dev
# または
npm run dev
# または
yarn dev
# または
bun dev
```

4. ブラウザで以下のURLにアクセスします。

[http://localhost:3000](http://localhost:3000)

## 開発ガイド

メインのエントリーポイントは `app/page.tsx` です。ここからトップページのレイアウトやセクションを編集できます。

- ページを編集すると、保存後すぐにブラウザがホットリロードされ、変更内容を確認できます。
- 共通レイアウトやメタ情報などは `app/layout.tsx`（存在する場合）で管理します。
- 再利用可能な UI コンポーネントは `app` 配下、もしくは `components` ディレクトリ（作成している場合）にまとめておくと保守しやすくなります。

フォントは Next.js 純正の `next/font` を使い、Vercel が提供する Geist フォントを自動最適化して読み込んでいます。

## 環境変数

機密情報や環境ごとに異なる設定値は `.env` に定義します。テンプレートとして `.env.example` を用意しています。

1. `.env.example` をコピーして `.env` を作成します。

```bash
cp .env.example .env
```

2. `.env` 内の値を自身の環境に合わせて編集します。

`.env` は Git にコミットしないよう `.gitignore` で除外されています。

## デプロイ

本プロジェクトは、Vercel へのデプロイを想定しています。Next.js 向けに最適化されたホスティング環境のため、設定もシンプルです。

1. Vercel アカウントを作成 / ログインします。
2. この GitHub リポジトリを Vercel 上でインポートします。
3. ビルドコマンド・出力ディレクトリなどは、Next.js プロジェクトであれば基本的にデフォルト設定のままで問題ありません。
4. 環境変数が必要な場合は、Vercel の「Environment Variables」に `.env` と同じキー名で登録します。

デプロイが完了すると、Vercel から本番用 URL およびプレビュー URL が自動的に発行されます。

## スクリプト

`package.json` で定義されている主なスクリプトは以下の通りです（必要に応じて実際の内容に合わせて編集してください）。

- `dev`: 開発サーバーを起動
- `build`: 本番ビルドを作成
- `start`: ビルド済みアプリケーションを起動
- `lint`: ESLint による静的解析を実行

```bash
pnpm dev      # 開発
pnpm build    # ビルド
pnpm start    # 本番起動
pnpm lint     # Lint チェック
```

## プロジェクト構成（概要）

実際の構成に合わせて、必要なものだけ残して編集してください。

- `app/` – ページやレイアウト、ルーティング関連
- `public/` – 画像やアイコンなどの静的ファイル
- `scripts/` – ビルドやデプロイ補助用のスクリプト類
- `eslint.config.mjs` – ESLint の設定
- `next.config.ts` – Next.js の設定
- `tsconfig.json` – TypeScript の設定
- `pnpm-workspace.yaml` – ワークスペース設定（モノレポ構成の場合）

## コントリビューション

このリポジトリは主に個人ポートフォリオ用途ですが、改善案やバグ報告などがあれば Issue や Pull Request を歓迎します。

1. Fork & clone
2. 新しいブランチを作成
3. 修正を加えて `pnpm lint` / `pnpm build` などで動作確認
4. Pull Request を作成

## ライセンス

ライセンス形態を決めている場合はここに記載してください。例：

- MIT License
- All rights reservedThis is a [Next.js](https://nextjs.org) project bootstrapped with [`create-next-app`](https://nextjs.org/docs/app/api-reference/cli/create-next-app).

## Getting Started

First, run the development server:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
# or
bun dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `app/page.tsx`. The page auto-updates as you edit the file.

This project uses [`next/font`](https://nextjs.org/docs/app/building-your-application/optimizing/fonts) to automatically optimize and load [Geist](https://vercel.com/font), a new font family for Vercel.

## Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js) - your feedback and contributions are welcome!

## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/app/building-your-application/deploying) for more details.
