### apache2サーバーの立ち上げ
1. apacheサーバーのインストール
```sh
sudo apt install apache2
```
- サーバーの立ち上げ
```sh
sudo systemctl start apache2
```
- サーバーの立ち上げの確認
```sh
sudo systemctl status apache2
```
![apache_status](image/apache2_status)
2. htmlの作成(defaultもあるが分かりづらい)
```sh
sudo vi /var/www/html/index.html
```
- htmlの内容
```index.html
<!DOCTYPE html>
<p>Hello,World!</p>
```
3. serverの設定を追記
```sh
sudo vim /etc/apache2/apache2.conf
```
- 以下の内容を追記
```txt
    AuthType Basic
    AuthName "Basic Authentication"
    AuthUserFile /etc/apache2/.htpasswd
    require valid-user
```
![apach2_conf](./image/apach2_conf)

4. user登録
> [今回はtestユーザで作成するよ]
> htpasswd -c \[filepath] [user]
```sh
sudo htpasswd -c /etc/apache2/.passwd test
```
