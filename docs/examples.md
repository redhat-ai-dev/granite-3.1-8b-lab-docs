## Usage Examples

##### **Using Curl**

```
curl -X 'POST' \
    'https://<model-server-host>.com/v1/completions' \
    -H 'accept: application/json' \
    -H 'Content-Type: application/json' \
    -H 'Authorization: Bearer <YOUR_API_KEY>' \
    -d '{
    "model": "granite-31-8b-lab",
    "prompt": "San Francisco is a",
    "max_tokens": 15,
    "temperature": 0
}'
```

##### **Python**

```python
import requests
import urllib3
import numpy as np
import json

API_URL = "https://<model-server-host>.com"
API_KEY = "***************************"

input = ["San Francisco is a"]

completion = requests.post(
    url=API_URL+'/v1/completions',
    json={
      "model": "granite-31-8b-lab",
      "prompt": "San Francisco is a",
      "max_tokens": 15,
      "temperature": 0
    },
    headers={'Authorization': 'Bearer '+API_KEY}
).json()

print(completion)
```