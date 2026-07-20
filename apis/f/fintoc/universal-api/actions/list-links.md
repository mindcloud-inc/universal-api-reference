# Fintoc: List Links

Retrieves links from Fintoc.

```
GET https://connect.mindcloud.co/v1/universal/fintoc/latest/actions/list-links
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fintoc `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fintoc/latest/actions/list-links?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fintoc/latest/actions/list-links?${params}`, {
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
      "accounts": [
        {}
      ],
      "active": true,
      "created_at": "string",
      "holder_id": "string",
      "holder_type": "string",
      "id": "string",
      "institution": {},
      "link_token": "https://example.com",
      "mode": "string",
      "object": "string",
      "status": "string",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accounts` | array<object> |  |
| `active` | boolean |  |
| `created_at` | string |  |
| `holder_id` | string |  |
| `holder_type` | string |  |
| `id` | string |  |
| `institution` | object |  |
| `link_token` | string |  |
| `mode` | string |  |
| `object` | string |  |
| `status` | string |  |
| `username` | string |  |

## Native endpoint

Through the native Fintoc API, this operation is `GET /v1/links` (base URL `https://api.fintoc.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-links.md) for the provider-specific parameters and requirements.

