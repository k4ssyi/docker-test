DockerでRuby on Railsの開発環境をするテスト

使用したコマンド
```
// Dockerfileからイメージの作成docker build
$ docker build -t devloper_name/pjt_name .
// -t:タグ・名前をつける

// buildしたイメージをコンテナ化
$ docker run --rm -i -t devloper_name/pjt_name -v <ローカルパス>:<マウント先パス>
// --rm:コンテナ停止時に自動的に削除
// -p:コンテナ外からのアクセス:コンテナ側のポート番号
// -i:ホストの入力をコンテナの標準出力をつなげる
// -t:コンテナの標準出力とホストの出力をつなげる
// -v:volumeをマウントする場合につける

// イメージの確認
$ docker images

// コンテナの確認
$ docker ps -a # -aをつけると停止しているコンテナも表示する

// コンテナの停止
$ docker stop <コンテナID>

// ゴミを削除
$ docker rm <コンテナID> <コンテナID> .... # コンテナを削除、複数指定可
$ docker rmi <イメージID> <イメージID>　.... # イメージを削除、複数指定可
```
