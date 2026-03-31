# システム概要：Re:Spec

## 1. システムの目的
Re:Specは、AI駆動開発（AIDD）時代における仕様書管理プラットフォームである。従来のウォーターフォール開発で作成されたドキュメントと、現代のAI駆動開発環境を構造化された仕様書（スペック）で接続し、開発プロセス全体の効率化と品質向上を実現する。

## 2. スコープ
本システムは、Notion、Word、PDF、GitHubリポジトリなど、多様なソースから仕様情報を集約・管理する。PM、開発者、QAなど、開発に関わる全てのステークホルダーが同一プラットフォーム上で仕様書を管理できる環境を提供する。llllllkkkkkkkkk

## 3. 用語定義
*   **AIDD (AI Driven Development)**: AIを活用した開発手法。
*   **FDE (Forward Deployed Engineer)**: 導入支援を行うエンジニア。
*   **TAM/SAM/SOM**: 市場規模指標（Total Addressable Market / Serviceable Available Market / Serviceable Obtainable Market）。
*   **構造化データ**: AIが読み取り・解析可能な形式に変換された仕様情報。

## 4. 全体構成

### 4.1 システムの役割
Re:Specは、以下の3つの要素を仲介するハブおよびプラットフォームとして機能する。
1.  **古いシステム（ウォーターフォール）**: 既存の仕様書資産。
2.  **構造化された仕様書（スペック）**: AI可読な中間データ。
3.  **AI駆動開発（Claude Code等）**: 最新の開発環境。

### 4.2 主要機能
*   **仕様書の自動変換**: 古い仕様書（Word/PDF等）をAI可読な構造化データへ変換。
*   **AI品質レビュー**: 8観点AIインスペクションによる仕様書の漏れ指摘および修正。
*   **GitHub連携**: 構造化データのGitHubへのプッシュおよびコード変更検知による仕様書自動更新。
*   **リポジトリ解析**: 既存コードから仕様書を自動生成。
*   **通知機能**: 仕様と実装の乖離をNotion/Slack/Teamsへアラート通知。
*   **マイクロサービス設計**: 各機能は疎結合なマイクロサービスとして構成。

### 4.3 連携フロー
ローカルのAIDD環境（Claude Code + Git）とGitHub、およびRe:Specプラットフォームが連携し、以下のサイクルを実現する。
1.  **INPUT**: Notion PRD、Word、PDF、GitHub Repoの取り込み。
2.  **プロセス**: 構造化、AIインスペクション、コード同期、通知。
3.  **OUTPUT**: Word、PDF、SPEC_template、監査証跡JSON、Notionステータス更新。

### 4.4 ビジネスモデル
*   **SaaS**: フリーミアムモデルを採用（Free/Starter/Business/Enterprise）。
*   **Professional Services**: FDEによる導入支援（Quick Start/Enterprise導入/Strategic Partner）。