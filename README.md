# Home Assistant Custom Components

このリポジトリには、Home Assistant用のカスタムコンポーネントが2つ含まれています。

## 📦 含まれているインテグレーション

### CUPS (OpenPrinting) - v1.1.0

[![hacs_badge](https://img.shields.io/badge/HACS-Custom-orange.svg)](https://github.com/hacs/integration)

CUPS (Common UNIX Printing System) プリンターをHome Assistantに統合します。

**機能:**
- プリンターの状態監視
- インク/トナーレベルの表示
- 印刷ジョブの管理
- バイナリセンサーとセンサーのサポート
- Zeroconf による自動検出対応

**必要要件:**
- Home Assistant 2024.1.0 以降
- CUPS サーバーへのネットワークアクセス
- pyipp>=0.9.0（自動インストール）

**設定:** UI から設定可能（Config Flow対応）

---

### Nature Remo - v1.0.1

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
- aiohttp>=3.8.0（自動インストール）

**設定:** UI から設定可能（Config Flow対応）

## 🔧 インストール方法

### 推奨：手動インストール

このリポジトリには2つのインテグレーションが含まれているため、**手動インストールを推奨**します。

#### 方法1: Gitでクローン

```bash
# リポジトリをクローン
git clone https://github.com/98kuwa036/homeasistant.git

# custom_componentsフォルダをHome Assistantの設定ディレクトリにコピー
cp -r homeasistant/custom_components/* /path/to/homeassistant/config/custom_components/

# Home Assistantを再起動
```

#### 方法2: ダウンロード

1. このリポジトリの [最新リリース](https://github.com/98kuwa036/homeasistant/releases) またはコードをダウンロード
2. ZIPファイルを解凍
3. `custom_components` フォルダ内の必要なインテグレーション（`cups` や `nature_remo`）を、Home Assistantの設定ディレクトリの `custom_components` フォルダにコピー
4. Home Assistantを再起動

### HACS経由でのインストール（制限あり）

⚠️ **注意**: HACSの制限により、このリポジトリをカスタムリポジトリとして追加すると、両方のインテグレーションが同時にインストールされます。個別にインストールすることはできません。

1. HACSを開く
2. 「Integrations」をクリック
3. 右上のメニュー（︙）から「Custom repositories」を選択
4. 以下の情報を入力：
   - リポジトリURL: `https://github.com/98kuwa036/homeasistant`
   - カテゴリー: `Integration`
5. インテグレーションをインストール
6. Home Assistantを再起動

## 📝 設定方法

インストール後、以下の手順で各インテグレーションを設定します。

### CUPS の設定

1. Home Assistantの「設定」→「デバイスとサービス」を開く
2. 「統合を追加」をクリック
3. "CUPS"を検索して選択
4. CUPSサーバーのホスト名またはIPアドレスを入力
5. プリンターが自動的に検出されます

または、Zeroconfが有効な場合、ネットワーク上のCUPSプリンターが自動的に検出されます。

### Nature Remo の設定

1. [Nature Remo API](https://home.nature.global/) でアクセストークンを取得
2. Home Assistantの「設定」→「デバイスとサービス」を開く
3. 「統合を追加」をクリック
4. "Nature Remo"を検索して選択
5. APIトークンを入力
6. デバイスが自動的に検出されます

## 💬 サポート

問題が発生した場合は、[Issues](https://github.com/98kuwa036/homeasistant/issues) でご報告ください。

## 📄 ライセンス

このプロジェクトに含まれる各コンポーネントは、それぞれのライセンスに従います。

## 🤝 貢献

プルリクエストを歓迎します。大きな変更の場合は、まず Issue を開いて変更内容を議論してください。
