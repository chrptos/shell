## user追加
```
useradd
```
### オプションなしで実行すると、new_userというユーザーとグループが作成される
```
useradd new_user
```

## 作成されたユーザー一覧
```
less /etc/passwd
new_user:x:1003:1003::/home/new_user/:/bin/bash
```
ユーザー名:暗号化パスワード:ユーザーID:グループID:コメントID:ホームディレクトリ:ログインシェル
### 暗号化されたユーザーパスワード
```
/etc/shadow
```

## 作成されたグループ一覧
```
less /etc/group
new_user:x:1003:
```
グループ名:暗号化されたパスワード:グループID:ユーザーリスト
### 暗号化されたグループパスワード
```
/etc/gshadow
```

## useradd オプション
-d ディレクトリ
-s シェル
-g グループ指定
```
useradd new_user -g new_group
```

## chown(-R: 再帰)
```
chown <所有user>:<所有group>
```

## chmod(-R: 再帰) r:w:x 4:2:1
```
chmod 所有ユーザー:所有グループ:それ以外のユーザー
chmod 700 test.txt
```
所有ユーザーのみ読み込み書き込み実行権限を持つ
