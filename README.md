# Python Library Template

本リポジトリは、パッケージマネージャーに `uv`、Linterおよびフォーマッタに `Ruff` を採用した汎用ライブラリ開発用のテンプレートです。

`Ruff` とのエディタ上での競合（二重警告等）を回避するため、`.vscode/settings.json` にて `Pylance` の一部機能を無効化する設定が適用されています。これにより、型の解決は `Pylance`、コード解析と整形は `Ruff` が担う構成となっています。

## セットアップ

### 1. プロジェクトの作成
実行環境に合わせて、以下のいずれかの方法で新規リポジトリを用意してください。

**方法1: GitHubのテンプレート機能（ブラウザ操作）を利用する場合**
1. GitHub上の本リポジトリ画面右上にある **「Use this template」** をクリックし、**「Create a new repository」** を選択します。
2. 画面の指示に従って新規リポジトリを作成します。
3. 作成されたリポジトリをローカル環境にクローンし、ディレクトリを移動します。
```bash
git clone <作成した新規リポジトリのURL>
cd <新規リポジトリ名>
```

**方法2: Gitコマンドで手動クローンする場合**
```bash
git clone https://github.com/Tat1209/python-template.git <dir_name>
cd <dir_name>
rm -rf .git  # Windows環境の場合は rmdir /s /q .git
git init
```

### 2. 環境構築
以下の手順で、ローカル環境に使用するPythonバージョンを指定して環境を構築してください。

```bash
# 1. 使用するPythonバージョンの固定（.python-version の生成）
uv python pin 3.12

# 2. 依存関係の同期と仮想環境（.venv）の作成
uv sync
```
