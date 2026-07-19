# cpaw writeup
### Q1.[Misc] Test Problem
- 問題文にあるこれを入力
```text
cpaw{this_is_Cpaw_CTF}
```

### Q6.[Crypto] Classical Cipher
シーザー暗号とはアルファベットをずらすという暗号なのでcpawという文字がでてくるまでずらします。

> sedでは略記できない
- 文字列を置換する
```sh
echo fsdz{Fdhvdu_flskhu_lv_fodvvlfdo_flskhu} | tr "A-Za-z" "x-za-wX-ZA-W"
```
### Q7.[Reversing] Can you execute ?

- file タイプを確認する
```sh
file exec_me
```
- 権限がないので実行権限を付与
```sh
sudo chmod u+x exec_me
```
- fileを実行
```sh
./exec_me
```
### Q8.[Misc] Can you open this file ?
- fileタイプの確認
```sh
file open_me 
```
- documetと分かったので拡張子を変更する
```sh
mv open_me open_me.docx
```
### Q9.[Web] HTML Page
- serverが落とされてるので出来ない

### Q10.[Forensics] River
- 下記サイトでexif情報を確認<br>
[exif確認君](http://exif-check.org/)

### Q14.[PPC]並べ替えろ!
- pythonで並び替える
```python
l = [15,1,93,52,66,31,87,0,42,77,46,24,99,10,19,36,27,4,58,76,2,81,50,102,33,94,20,14,80,82,49,41,12,143,121,7,111,100,60,55,108,34,150,103,109,130,25,54,57,159,136,110,3,167,119,72,18,151,105,171,160,144,85,201,193,188,190,146,210,211,63,207]

bigl = sorted(l,revese=True)

sl = [str(n) for n in bigl]
print(''.join(sl))
```
---
