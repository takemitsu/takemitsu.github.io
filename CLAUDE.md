# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## プロジェクト概要

GitHub Pagesを使用したシンプルな静的ウェブサイトプロジェクト。個人のホームページ・ポートフォリオサイトとして機能する単一のHTMLファイルで構成されています。

## アーキテクチャ

- **静的サイト**: Pico CSS v2を使用した単一ファイルのHTMLウェブサイト
- **デプロイ**: GitHub Pages（リポジトリ名 `takemitsu.github.io` に基づく）
- **言語**: 日本語（HTMLのlang="ja"）
- **フレームワーク**: CDN経由でPico CSS v2を使用（ビルドプロセス不要）
- **フォント**: JetBrains Mono（Google Fonts経由）
- **テーマ**: ライト/ダーク/自動切り替え対応
- **レスポンシブ**: モバイルファースト設計、ハンバーガーメニュー実装

## ファイル構造

```
/
├── index.html          # Bootstrapナビバーとコンテンツを含むメインページ
└── CLAUDE.md          # この説明ファイル
```

## 開発方法

ビルドプロセスが不要な静的ウェブサイトです。`index.html`への変更は GitHub Pages を通じて直接デプロイされます。

### コーディング規約
- **必須**: git push前にはHTMLフォーマッターを実行する（Prettierを使用: `npx prettier --write index.html`）
- ビルドプロセスが不要な方法でコードを書く（シンプルに保つ）
- 外部依存はCDN経由で読み込む
- JavaScriptは最小限に留める（UIインタラクションのみ）

### ローカル開発
- ローカルテスト用には `index.html` を直接ブラウザで開く
- 必要であればシンプルなHTTPサーバーを使用: `python -m http.server 8000`

### デプロイ手順
1. HTMLフォーマッターでコードを整形
2. `master` ブランチに変更をプッシュ
3. GitHub Pages がルートディレクトリから自動的にデプロイ