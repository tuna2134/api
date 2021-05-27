# qrcodeapi

### 作成

パラメータ値

名前:text 例:google.com<-文なら何でもいい

戻り値

名前:url 例:qrcode.dmssite.cf/api/create/<token>

### 読み取り

comming soon...

### example code
```python
import requests
import json

token=#your token
text=input('qrcodeにしたいtextを入力してください')

print("通信中")

query={
   "text": text
   }
res=requests.get(f'qrcode.dmssite.cf/api/create/{token}', params=query)
api=json.loads(res.text)
print(api["url"])
