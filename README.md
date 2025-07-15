# Claude Code 共通設定

このリポジトリには、Claude Code を使用する際の共通設定とドキュメントが含まれています。

## 📁 ファイル構成

### 設定ファイル
- **`CLAUDE.md`** - プロジェクト設定とガイドライン
- **`github_config.json.template`** - GitHub設定のテンプレート
- **`.gitignore`** - Git除外ファイル設定

### システムファイル
- **`notification_system.py`** - 通知システム
- **`.claude-code/`** - Claude Code hooks設定

## 🚀 セットアップ手順

### 1. GitHub設定
```bash
# テンプレートをコピーして設定
cp github_config.json.template github_config.json
# 実際の値に編集
nano github_config.json
```

### 2. 通知システム
```bash
# 通知システムをホームディレクトリにコピー
cp notification_system.py ~/
# 実行権限を付与
chmod +x ~/notification_system.py
```

### 3. Claude Code hooks
```bash
# hooksディレクトリをコピー
cp -r .claude-code ~/
# 実行権限を付与
chmod +x ~/.claude-code/hooks/*
```

## 🔧 機能

### 通知システム
- Claude Code作業完了時のポップアップ通知
- マルチディスプレイ対応
- カスタマイズ可能な表示設定

### Git設定
- Personal Access Token による認証
- 自動コミットメッセージ設定
- セキュアな設定管理

### Hooks
- 作業完了時の自動通知
- ユーザー確認待ち状態の検知

## 📋 使用方法

新しいプロジェクトを始める際は、このリポジトリの設定を参考にしてClaude Code環境をセットアップしてください。

## 🛡️ セキュリティ

- `github_config.json` は `.gitignore` で除外されています
- Personal Access Token は最小権限で設定してください
- 定期的にトークンを更新することを推奨します

## 📝 更新履歴

- 2025-07-15: 初期リポジトリ作成
- 通知システム実装
- マルチディスプレイ対応追加