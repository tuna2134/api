#短縮URL

https://shorturl.dmssite.cf/api/<あなたのTOKEN>

レート制限:1分あたり100回まで

パラメーター

名前:url 例:https://google.com

戻り値:

名前:short_url 例:tinyurl.com/dwjdnwic

#example code
```python
import requests
import json

token=#your token
url=input('URLを入力してください')

query={
   "url": url
   }
res=requests.get(f'shorturl.dmssite.cf/api/{token}', params=query)
api=json.loads(res.text)
print(api["short_url"])
```
