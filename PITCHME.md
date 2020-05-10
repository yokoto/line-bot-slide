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
# 新しくconfig/credentials.yml.encを作成する。
# 開いたファイルを保存して終了(:wq)すると、新しくcredentials.yml.encとmaster.keyが作成される。
$ EDITOR=vim rails credentials:edit
$ git add .
$ git commit -m "init credentials and master.key"
$ heroku config:set RAILS_MASTER_KEY=${master.keyの中身をペースト}


$ heroku push origin master
$ heroku config:set LINE_CHANNEL_SECRET=${チャネルシークレットをペースト}
$ heroku config:set LINE_CHANNEL_TOKEN=${チャネルアクセストークンをペースト}
```


---


### 3枚目のスライド


---


### 4枚目のスライド
