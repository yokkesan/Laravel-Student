# Laravel Sample

## 必要なもの

事前に以下をインストールしてください。

- Docker Desktop
- Git

---

## プロジェクト取得

リポジトリを clone します。

bash git clone リポジトリURL

プロジェクトへ移動します。

bash cd Laravel-student

---

## Docker 起動

Docker コンテナを起動します。

bash 
docker compose up --build

起動できたらDocker内のappコンテナに入ります。
docker exec -it laravel-student-app-1 bash

---

## Laravel 初期設定（初回のみ）

依存パッケージをインストールします。

composer install

.env ファイルを作成します。

cp .env.example .env

アプリケーションキーを生成します。

php artisan key:generate

データベースのテーブルを作成します。

php artisan migrate

---

## 動作確認

ブラウザで下記へアクセスしてください。

http://localhost:8001

Laravel の初期画面が表示されれば成功です。

---

## 停止方法

コンテナ停止：

bash docker compose down

## デバックツール使用するなら
composer require barryvdh/laravel-debugbar --dev

## キャッシュクリアコマンド