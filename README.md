# Home Assistant Custom Components

このリポジトリには、Home Assistant用のカスタムコンポーネントが含まれています。

## インストール方法

### HACS経由でのインストール

1. HACSを開く
2. 「Integrations」をクリック
3. 右上のメニューから「Custom repositories」を選択
4. リポジトリURL `https://github.com/98kuwa036/homeasistant` を追加
5. カテゴリーを「Integration」として選択
6. インストールしたいコンポーネントを検索してインストール

### 手動インストール

1. このリポジトリをクローンまたはダウンロード
2. `custom_components` フォルダを Home Assistant の設定ディレクトリにコピー
3. Home Assistant を再起動

## 含まれているコンポーネント

### CUPS (OpenPrinting)

[![hacs_badge](https://img.shields.io/badge/HACS-Custom-orange.svg)](https://github.com/hacs/integration)

CUPS (Common UNIX Printing System) プリンターをHome Assistantに統合します。

**機能:**
- プリンターの状態監視
- インク/トナーレベルの表示
- 印刷ジョブの管理
- バイナリセンサーとセンサーのサポート

**必要要件:**
- Home Assistant 2024.1.0 以降
- CUPS サーバーへのネットワークアクセス

**設定:**
- UI から設定可能（Config Flow対応）
- Zeroconf による自動検出対応

### Nature Remo

[![hacs_badge](https://img.shields.io/badge/HACS-Custom-orange.svg)](https://github.com/hacs/integration)

Nature Remo スマートリモコンをHome Assistantに統合します。

**機能:**
- エアコンの制御（Climate）
- 照明の制御（Light）
- リモコンボタンの送信（Remote）
- センサーデータの取得（温度、湿度、照度）
- スイッチの制御

**必要要件:**
- Home Assistant 2024.1.0 以降
- Nature Remo アカウントとAPIトークン
- インターネット接続（クラウドポーリング）

**設定:**
- UI から設定可能（Config Flow対応）

## サポート

問題が発生した場合は、[Issues](https://github.com/98kuwa036/homeasistant/issues) でご報告ください。

## ライセンス

このプロジェクトに含まれる各コンポーネントは、それぞれのライセンスに従います。

## 貢献

プルリクエストを歓迎します。大きな変更の場合は、まず Issue を開いて変更内容を議論してください。
