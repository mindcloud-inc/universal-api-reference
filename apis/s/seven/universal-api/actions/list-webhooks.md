# Seven: List Webhooks

Retrieves webhooks from Seven.

```
GET https://connect.mindcloud.co/v1/universal/seven/latest/actions/list-webhooks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Seven `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seven/latest/actions/list-webhooks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seven/latest/actions/list-webhooks?${params}`, {
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
      "code": "string",
      "hooks": {
        "created": "2026-05-07T12:00:00.000Z",
        "enabled": true,
        "event_filter": "string",
        "event_type": "string",
        "headers": "string",
        "id": "string",
        "request_method": "string",
        "target_url": "https://example.com"
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
| `code` | string |  |
| `hooks` | array<object> |  |
| `hooks.created` | date |  |
| `hooks.enabled` | boolean |  |
| `hooks.event_filter` | string |  |
| `hooks.event_type` | string |  |
| `hooks.headers` | string |  |
| `hooks.id` | string |  |
| `hooks.request_method` | string |  |
| `hooks.target_url` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Seven API, this operation is `GET /hooks` (base URL `https://gateway.seven.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-webhooks.md) for the provider-specific parameters and requirements.

