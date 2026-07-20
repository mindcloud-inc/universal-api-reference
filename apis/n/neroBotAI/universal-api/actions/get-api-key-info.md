# NeroBot AI: Get API Key Info

Retrieves API key info from NeroBot AI.

```
GET https://connect.mindcloud.co/v1/universal/neroBotAI/latest/actions/get-api-key-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NeroBot AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/neroBotAI/latest/actions/get-api-key-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/neroBotAI/latest/actions/get-api-key-info?${params}`, {
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
      "code": 1,
      "data": {
        "expired_at": "string",
        "remaining_credits": 1,
        "status": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `data` | object |  |
| `data.expired_at` | string |  |
| `data.remaining_credits` | number |  |
| `data.status` | string |  |

## Native endpoint

Through the native NeroBot AI API, this operation is `GET /biz/api/apikey` (base URL `https://api.nero.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-api-key-info.md) for the provider-specific parameters and requirements.

