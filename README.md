# Python
```py
import requests as r

# creating user
d = r.post("https://razdor/chat/v1/user/create", json={"username": "some username", "password": "some password"})
print(d.json())
# you should get the op "Created." with an ID in the json
print(d.json()['id'])

# logging in / generating an auth key
d = r.post("https://razdor/chat/v1/user/create", json={"auth": "your password"})
# you should get json containing 'authentication' (your auth key / token)
# this is what you use for authentication for needed endpoints.

# will add more later
```
