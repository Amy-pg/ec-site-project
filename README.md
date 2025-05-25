# EC Site Project

## 概要

このプロジェクトは、2025年5月25日に@qumaiuさんが投稿したXポスト（[こちら](https://x.com/qumaiu/status/1926457465987608968)）の内容を再現することを目的としています。具体的には、Claude CodeとGitHub Actionsを活用して、議事録から要件定義ドキュメントを自動生成するワークフローを構築します。

## 背景

@qumaiuさんのポストでは、以下の流れでAI駆動開発を実現しています：
- 会議の議事録を録音し、文字起こしする。
- 文字起こしした内容をGitHubにコミット。
- Claude Codeに指示を出し、GitHub Actionsを動作させる。
- 移動中にGitHub Actionsが処理を行い、帰社時には要件定義ドキュメントが完成。

このプロジェクトでは、上記のワークフローを再現し、「新しいECサイトの開発プロジェクト」を例として、議事録（`meeting-notes.md`）から要件定義ドキュメント（`requirements.md`）を生成するプロセスを試みます。

## プロジェクト構造

- `meeting-notes.md`: デモ用の議事録（新しいECサイト開発に関する会議の文字起こし）。
- `requirements.md`: Claude Codeで生成される要件定義ドキュメント。
- `.github/workflows/claude.yml`: GitHub Actionsのワークフローファイル。
- `docs/template.md`: 要件定義ドキュメントのテンプレート（オプション）。

## セットアップ方法

1. AnthropicのAPIキー（`ANTHROPIC_API_KEY`）を取得し、リポジトリのSecretsに設定。
2. Claude GitHub Appをリポジトリにインストール。
3. `meeting-notes.md`を更新し、プッシュしてGitHub Actionsを実行。
4. 生成された`requirements.md`を確認。

詳細な手順は、[ワークフローの設定ドキュメント](.github/workflows/claude.yml)を参照してください。

## 目的

- AI駆動開発の一例として、Claude Codeを活用した自動ドキュメント生成を体験する。
- 「Project as Code」のアプローチを学び、上流工程の効率化を目指す。

## ライセンス

MIT License