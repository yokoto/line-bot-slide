### LINEbotアプリを作ってみよう

横田 俊博
2020年5月11日


---


### 2枚目のスライド


```
$ heroku login
$ heroku create

# これ(Railsの秘匿情報管理)をやらないとpushに失敗する。
$ rm config/credentials.yml.enc
$ EDITOR=vim rails credentials:edit # 開いたファイルは保存して終了する。新しくcredentials.yml.encとmaster.keyが作成される。
$ git add .
$ git commit -m "init credentials and master.key"
$ heroku config:set RAILS_MASTER_KEY=${master.keyの中身をペースト}


$ heroku push origin master
$ heroku config:set LINE_CHANNEL_SECRET=${チャネルシークレットをペースト}
$ heroku config:set LINE_CHANNEL_TOKEN=${チャネルアクセストークンをペースト}
+++


### 3枚目のスライド


---


### 4枚目のスライド
