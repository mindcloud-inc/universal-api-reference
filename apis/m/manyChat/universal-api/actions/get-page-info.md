# ManyChat: Get Page Info

Retrieves connected page details from ManyChat.

```
GET https://connect.mindcloud.co/v1/universal/manyChat/latest/actions/get-page-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ManyChat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/manyChat/latest/actions/get-page-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/manyChat/latest/actions/get-page-info?${params}`, {
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
      "about": {},
      "avatarLink": {},
      "category": {},
      "description": {},
      "id": {},
      "isPro": true,
      "name": "Ava Chen",
      "timezone": "string",
      "username": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `about` | object |  |
| `avatarLink` | object |  |
| `category` | object |  |
| `description` | object |  |
| `id` | object |  |
| `isPro` | boolean |  |
| `name` | string |  |
| `timezone` | string |  |
| `username` | object |  |

## Native endpoint

Through the native ManyChat API, this operation is `GET /fb/page/getInfo` (base URL `https://api.manychat.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-page-info.md) for the provider-specific parameters and requirements.

