# Python Library Template

本リポジトリは、パッケージマネージャーに `uv`、Linterおよびフォーマッタに `Ruff` を採用した汎用ライブラリ開発用のテンプレートです。

`Ruff` とのエディタ上での競合（二重警告等）を回避するため、`.vscode/settings.json` にて `Pylance` の一部機能を無効化する設定が適用されています。これにより、型の解決は `Pylance`、コード解析と整形は `Ruff` が担う構成となっています。

## セットアップ

以下の手順で、ローカル環境に使用するPythonバージョンを指定して環境を構築してください。

```bash
# 1. 使用するPythonバージョンの固定（.python-version の生成）
uv python pin 3.12

# 2. 依存関係の同期と仮想環境（.venv）の作成
uv sync
```
