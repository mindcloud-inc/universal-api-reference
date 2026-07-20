# jo4.io: List API Keys



```
GET https://connect.mindcloud.co/v1/universal/jo4io/latest/actions/list-api-keys
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a jo4.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jo4io/latest/actions/list-api-keys?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jo4io/latest/actions/list-api-keys?${params}`, {
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
      "createdTime": 1,
      "description": "string",
      "enabled": true,
      "expired": true,
      "expiresAt": 1,
      "id": 1,
      "keyPrefix": "string",
      "lastUsedAt": 1,
      "lastUsedIp": "string",
      "modifiedTime": 1,
      "name": "Ava Chen",
      "scopes": [
        "string"
      ],
      "slug": "string",
      "useCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdTime` | number |  |
| `description` | string |  |
| `enabled` | boolean |  |
| `expired` | boolean |  |
| `expiresAt` | number |  |
| `id` | number |  |
| `keyPrefix` | string |  |
| `lastUsedAt` | number |  |
| `lastUsedIp` | string |  |
| `modifiedTime` | number |  |
| `name` | string |  |
| `scopes` | array<string> |  |
| `slug` | string |  |
| `useCount` | number |  |

## Native endpoint

Through the native jo4.io API, this operation is `GET /protected/api-keys` (base URL `https://jo4-api.jo4.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-api-keys.md) for the provider-specific parameters and requirements.

