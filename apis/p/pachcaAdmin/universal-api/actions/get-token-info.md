# Pachca (Admin): Get Token Info

Retrieves token information from the Pachca Admin API.

```
GET https://connect.mindcloud.co/v1/universal/pachcaAdmin/latest/actions/get-token-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pachca (Admin) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pachcaAdmin/latest/actions/get-token-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pachcaAdmin/latest/actions/get-token-info?${params}`, {
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
      "data": {
        "createdAt": "string",
        "expiresIn": {},
        "id": 1,
        "lastUsedAt": "string",
        "name": "Ava Chen",
        "revokedAt": {},
        "scopes": [
          "string"
        ],
        "token": "string",
        "userId": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.createdAt` | string |  |
| `data.expiresIn` | object |  |
| `data.id` | number |  |
| `data.lastUsedAt` | string |  |
| `data.name` | string |  |
| `data.revokedAt` | object |  |
| `data.scopes[]` | string |  |
| `data.token` | string |  |
| `data.userId` | number |  |

## Native endpoint

Through the native Pachca (Admin) API, this operation is `GET /oauth/token/info` (base URL `https://api.pachca.com/api/shared/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-token-info.md) for the provider-specific parameters and requirements.

