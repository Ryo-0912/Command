**scpコマンド**はローカルからリモートへファイルを渡したい(移動したい)時に使う。

```php
scp -i ~/.ssh/秘密鍵 /Users/氏名/bridge-d540d-c8e276592470.json remote.development@34.84.252.27:/home/remote.development
```

※ローカルからリモートへファイルを渡したいので、秘密鍵は必須p

ローカルにある`/Users/氏名`にある`bridge-d540d-c8e276592470.json`ファイルを、

リモートの`remote` ディレクトリ配下に移動させる

```php
scp -i ~/.ssh/秘密鍵 /Users/andouryou/bridge-d540d-c8e276592470.json A@34.84.252.27:/home/remote.development/usr
```

ローカルにある`/Users/氏名`にある`bridge-d540d-c8e276592470.json`ファイルを、

リモートの`remote.development/usr` ディレクトリ配下に移動させる

**cpコマンド**はある環境にファイルを、同じ環境にある別のファイルにコピーしたい時に実行する。(ローカルからローカルへ or リモートからリモートへ)

```php
remote.development@remote-staging:~$ ls
**bridge-d540d-c8e276592470.json**

remote.development@remote-staging:~$ sudo cp bridge-d540d-c8e276592470.json /
ここでbridge-d540d-c8e276592470.jsonファイルを/(ルートディレクトリ)配下にコピーしている

remote.development@remote-staging:~$ ls
bridge-d540d-c8e276592470.json

remote.development@remote-staging:~$ cd /
remote.development@remote-staging:/$ ls
bin  boot  **bridge-d540d-c8e276592470.json**  dev  etc  home  lib  lib32  lib64  libx32  lost+found  media  mnt  opt  proc  root  run  sbin  snap  srv  sys  tmp  usr  var
```
