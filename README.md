# MCP Server Configuration for CLINE

## 概要
このリポジトリは、CLINE（AI アシスタントツール）でModel Context Protocol (MCP) サーバーを利用するための設定とガイドラインを提供します。

## 前提条件

### 必要な環境
1. CLINE環境
   - VSCode拡張機能「Roo Code」（推奨）
   - または本家CLINEアプリケーション

2. 必要なツール
   - Node.js
   - npm

### 設定場所
MCPの設定ファイル（cline_mcp_settings.json）は以下の場所に配置します：

- Roo Code（VSCode拡張機能）の場合：
  ```
  /Users/(ユーザー名)/Library/Application Support/Code/User/globalStorage/rooveterinaryinc.roo-cline/settings/cline_mcp_settings.json
  ```

- 本家CLINEの場合：
  ```
  ~/Library/Application Support/Claude/claude_desktop_config.json
  ```

## プロジェクトの進化

### 1. 初期セットアップと動作確認
- 各MCPサーバーのインストールと動作確認
  - Filesystem Server
  - Brave Search
  - Puppeteer
  - GitHub
- 基本的な機能テスト実施

### 2. ファイル構成の最適化

#### 試行錯誤のプロセス
1. 最初のアプローチ
   - 多数のファイル（.env, スクリプトなど）を使用
   - 複雑な自動化を検討

2. 改善と簡素化
   - 不要な複雑さを排除
   - 設定の直接管理を採用

#### 最終的な構成

必要最小限の2ファイルに整理：

1. `.mcprules`
   - MCPサーバーの詳細設定とガイドライン
   - セットアップ手順
   - トラブルシューティング情報
   - セキュリティガイドライン

2. `.clinerules`
   - 基本的な参照情報
   - .mcprulesへのリンク
   - 設定ファイルの場所

## 利用可能なMCPサーバー

1. Filesystem Server
   - ファイルシステムへのアクセス
   - ファイル操作の自動化

2. Brave Search
   - Web検索機能の統合
   - 最新情報の取得

3. Puppeteer
   - Webブラウザの自動操作
   - スクリーンショットの取得

4. GitHub
   - リポジトリの操作
   - コード管理の自動化

## セットアップ方法

1. MCPサーバーのインストール
2. 設定ファイルの配置
3. CLINE/Roo Codeでの有効化

詳細な手順は `.mcprules` ファイルを参照してください。

## 学んだこと

1. シンプルさの重要性
   - 複雑な自動化より、明確で直接的な設定管理が有効
   - 不要なファイルやスクリプトの削除で保守性向上

2. セキュリティの考慮
   - 機密情報は集中管理
   - 設定ファイルの適切な配置

3. ドキュメントの重要性
   - 明確なガイドラインの提供
   - トラブルシューティング情報の整理

## 今後の展開

1. ユーザーガイドの充実
2. トラブルシューティング事例の蓄積
3. セキュリティガイドラインの継続的な改善

## 注意事項

- 設定ファイルにはトークンなどの機密情報が含まれるため、適切なアクセス制御が必要
- 定期的な設定の見直しと更新を推奨
- MCPサーバーの設定は、使用するCLINE環境に応じて適切な場所に配置してください