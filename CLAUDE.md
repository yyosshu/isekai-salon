# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## プロジェクト概要

「異世界転生サロン」の単一ページHTMLウェブサイト。5000万円で異世界転生体験を提供するという架空のサービスのランディングページです。

## アーキテクチャ

- **単一HTMLファイル**: プロジェクト全体が一つの`index.html`ファイルで構成され、HTML、CSS、JavaScriptが含まれています
- **自己完結型**: Google Fonts以外の外部依存関係なし、すべてのスタイルとスクリプトがインライン
- **静的ウェブサイト**: ビルドプロセス、サーバーサイドコード、複雑なアーキテクチャなし
- **レスポンシブデザイン**: CSS Gridとレスポンシブテクニックでモバイル対応

## 技術スタック

- Pure HTML5
- インラインCSSとカスタムユーティリティクラス
- バニラJavaScriptによるインタラクション
- Google Fonts（Noto Sans JP、Playfair Display）

## 開発コマンド

静的HTMLファイルのため、ビルドコマンド、テストスクリプト、パッケージマネージャーは不要：

- **サイト表示**: `index.html`をブラウザで直接開く
- **ローカルサーバー**: `python -m http.server 8000` または `npx serve .`
- **編集**: HTMLファイルを直接編集

## 主要機能

- スムーススクロールナビゲーション
- Intersection Observer APIを使用したスクロールアニメーション
- FAQアコーディオン機能
- 2050年12月31日までのライブカウントダウンタイマー
- レスポンシブグリッドレイアウト
- mailtoリンクによるメール問い合わせフォーム

## コード構造

HTMLファイルは以下のセクションで構成：
- ヒーローセクション（メインCTA）
- ベネフィット・特徴セクション
- 比較表
- 価格セクション
- お客様の声
- FAQ
- 最終CTA

CSSクラスはユーティリティファーストアプローチに従い、`.benefit-card`、`.comparison-table`、`.testimonial`など複雑な要素にはセマンティックなコンポーネントクラスを使用。

## Git コミットルール

- コミットメッセージはシンプルに内容のみを記述
- Claude Codeの署名や追加情報は不要
- 例: "Initial commit: Add isekai salon landing page with documentation and gitignore"