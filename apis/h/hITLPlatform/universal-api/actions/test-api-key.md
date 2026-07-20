# HITL Platform: Test API Key



```
GET https://connect.mindcloud.co/v1/universal/hITLPlatform/latest/actions/test-api-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HITL Platform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hITLPlatform/latest/actions/test-api-key?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hITLPlatform/latest/actions/test-api-key?${params}`, {
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
      "account_status": "string",
      "api_key_id": "string",
      "email": "ava@example.com",
      "permissions": [
        [
          "string"
        ]
      ],
      "rate_limit": {
        "limit": 1,
        "remaining": 1,
        "reset_at": "2026-05-07T12:00:00.000Z"
      },
      "user_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account_status` | string |  |
| `api_key_id` | string |  |
| `email` | string |  |
| `permissions[]` | array<string> |  |
| `rate_limit.limit` | number |  |
| `rate_limit.remaining` | number |  |
| `rate_limit.reset_at` | date |  |
| `user_id` | string |  |

## Native endpoint

Through the native HITL Platform API, this operation is `GET /test` (base URL `https://api.hitl.sh/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/test-api-key.md) for the provider-specific parameters and requirements.

