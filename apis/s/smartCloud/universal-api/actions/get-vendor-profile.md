# 2Smart Cloud: Get vendor info



```
GET https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/get-vendor-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 2Smart Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/get-vendor-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/get-vendor-profile?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "avatar_url": "https://example.com",
      "category": "string",
      "created": "string",
      "id": 1,
      "is_blocked": true,
      "login": "string",
      "mqttCredentials": {},
      "updated": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avatar_url` | string |  |
| `category` | string |  |
| `created` | string |  |
| `id` | number |  |
| `is_blocked` | boolean |  |
| `login` | string |  |
| `mqttCredentials` | object |  |
| `updated` | string |  |

## Native endpoint

Through the native 2Smart Cloud API, this operation is `GET /vendor/profile` (base URL `https://cloud.2smart.com/robot/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-vendor-profile.md) for the provider-specific parameters and requirements.

