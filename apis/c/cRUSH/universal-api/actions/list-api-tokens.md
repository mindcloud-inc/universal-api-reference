# CRUSH: List API Tokens



```
GET https://connect.mindcloud.co/v1/universal/cRUSH/latest/actions/list-api-tokens
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CRUSH `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cRUSH/latest/actions/list-api-tokens?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cRUSH/latest/actions/list-api-tokens?${params}`, {
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
      "key": {
        "createdAt": "2026-05-07T12:00:00.000Z",
        "isRevoked": true,
        "lastUsedAt": "2026-05-07T12:00:00.000Z",
        "requestCount": 1,
        "tokenPrefix": "string",
        "userId": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `key.createdAt` | date | When the API token was created. |
| `key.isRevoked` | boolean | Whether the API token is revoked. |
| `key.lastUsedAt` | date | When the API token was last used. |
| `key.requestCount` | number | Number of requests made with the API token. |
| `key.tokenPrefix` | string | Redacted prefix of the API token. |
| `key.userId` | string | User ID that owns the API token. |

## Native endpoint

Through the native CRUSH API, this operation is `GET /tokens` (base URL `https://app.crushthememory.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-api-tokens.md) for the provider-specific parameters and requirements.

