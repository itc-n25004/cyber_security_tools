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
![apache_status](/home/n25004/Pictures/Screenshots/Screenshot From 2026-06-25 15-44-01.png)
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

```
