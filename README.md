# Apache Docker Project

このプロジェクトは、Dockerを使用してApacheウェブサーバーをセットアップします。`src`ディレクトリにあるシンプルなHTMLページを提供します。

## プロジェクト構造

```
apache-docker
├── src
│   └── index.html
├── Dockerfile
├── .dockerignore
└── README.md
```

- `src/index.html`：Apacheサーバーによって提供されるHTMLコンテンツが含まれています。このファイルを変更して独自のコンテンツを追加できます。
- `Dockerfile`：Dockerイメージをビルドするための指示が含まれており、Apacheのインストールや`src/index.html`の適切なディレクトリへの配置が行われます。
- `.dockerignore`：Dockerビルドプロセス中に無駄なファイルを含めないようにするために、無視するファイルやディレクトリを指定します。

## セットアップ手順

1. **リポジトリをクローンする**：
   ```
   git clone <repository-url>
   cd apache-docker
   ```

2. **Dockerイメージをビルドする**：
   ```
   docker build -t apache-docker .
   ```

3. **Dockerコンテナを実行する**：
   ```
   docker run -d -p 80:80 apache-docker
   ```

4. **ウェブページにアクセスする**：
   ウェブブラウザを開き、`http://localhost`に移動して提供されたHTMLページを表示します。

## 使用方法

`src/index.html`ファイルを変更して、Apacheサーバーによって表示されるコンテンツを変更できます。変更を加えた後、Dockerイメージを再ビルドし、コンテナを再起動して更新を確認してください。