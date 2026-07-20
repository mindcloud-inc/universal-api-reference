# Cloudflare Browser Run: Verify API Token

Verifies whether a Cloudflare API token works.

```
GET https://connect.mindcloud.co/v1/universal/cloudflareBrowserRun/latest/actions/verify-api-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudflare Browser Run `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudflareBrowserRun/latest/actions/verify-api-token?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudflareBrowserRun/latest/actions/verify-api-token?${params}`, {
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
      "errors": [
        {}
      ],
      "messages": [
        {}
      ],
      "result": {
        "expires_on": "2026-05-07T12:00:00.000Z",
        "id": "string",
        "status": "string"
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errors` | array<object> |  |
| `messages` | array<object> |  |
| `result` | object |  |
| `result.expires_on` | date |  |
| `result.id` | string |  |
| `result.status` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Cloudflare Browser Run API, this operation is `GET /accounts/:accountId/tokens/verify` (base URL `https://api.cloudflare.com/client/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-api-token.md) for the provider-specific parameters and requirements.

