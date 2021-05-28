# qrcodeapi

### 作成


取得用 URL:https://qrcode.dmssite.cf/api/create/<あなたのトークン>

パラメータ値

名前:text 例:google.com<-文なら何でもいい

戻り値

名前:url 例:https://qrcode.dmssite.cf/image/hwnegchsjsjdjsne

### 読み取り

取得用 URL:https://qrcode.dmssite.cf/api/read/<あなたのトークン>


パラメーター値

名前:url 例:https://qrcode.dmssite.cf/image/Fu9j3flypWQLWPEO<-画像 URL で OK

取得値:

名前:text 例:https://example.com


### example code(qrcode作成)
```python
import requests
import json

text=input('qrcodeにしたいtextを入力してください：')
token= #your token

print("通信中")

query={
  "text": text
}
res=requests.get(f'https://qrcode.dmssite.cf/api/create/{token}',params=query)
api=json.loads(res.text)
print(api["url"])```
