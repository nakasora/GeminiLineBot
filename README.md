# GeminiAPI LINE Bot アプリケーション

このリポジトリは Gemini API を使用した LINE Bot アプリケーションのソースコードを含んでいます。このドキュメントでは、アプリケーションの設定方法、デプロイ手順、および環境変数の設定方法について説明します。

## 概要

Gemini API を活用してLINE Bot を作成しました。

## 前提条件

- Python 3.11 以降
- Heroku アカウント
- LINE Developers アカウント
- Google Cloud Platform アカウント（Gemini API の利用に必要）

## 環境変数

このアプリケーションでは以下の環境変数を設定する必要があります：

- `GEMINI_API_KEY`: Gemini API の API キー
- `LINE_ACCESS_TOKEN`: LINE Bot のアクセストークン
- `LINE_CHANNEL_SECRET`: LINE Bot のチャネルシークレット

## ローカルでの実行方法

1. 必要なライブラリをインストールします：

```
pip install -r requirements.txt
```

2. 環境変数を設定します（Windows の場合）：

```
set GEMINI_API_KEY=your_gemini_api_key
set LINE_ACCESS_TOKEN=your_line_access_token
set LINE_CHANNEL_SECRET=your_line_channel_secret
```

Mac/Linux の場合：

```
export GEMINI_API_KEY=your_gemini_api_key
export LINE_ACCESS_TOKEN=your_line_access_token
export LINE_CHANNEL_SECRET=your_line_channel_secret
```

3. アプリケーションを実行します：

```
python gemini_line_bot.py
```

## デプロイ

Heroku へのデプロイ手順は以下の通りです：

1. Heroku にログインします（初めての場合はアカウントを作成します）。
2. Heroku CLI をインストールし、ローカルマシンでログインします：

```
heroku login
```

3. Heroku に新しいアプリケーションを作成します：

```
heroku create
```

4. Heroku に環境変数を設定します：

```
heroku config:set GEMINI_API_KEY=your_gemini_api_key
heroku config:set LINE_ACCESS_TOKEN=your_line_access_token
heroku config:set LINE_CHANNEL_SECRET=your_line_channel_secret
```

5. アプリケーションを Heroku にデプロイします：

```
git push heroku main
```

6. LINE Developers コンソールで、Heroku アプリの URL を Webhook URL として設定します。

これで、Heroku 上で LINE Bot が稼働します。

## ライセンス

[ライセンス名]を参照してください。

## 貢献

プロジェクトへの貢献についてのガイドラインは[CONTRIBUTING.md](CONTRIBUTING.md)を参照してください。
