# Anchor: List Browser Sessions

Retrieves browser sessions from Anchor.

```
GET https://connect.mindcloud.co/v1/universal/anchor/latest/actions/list-browser-sessions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Anchor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/anchor/latest/actions/list-browser-sessions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/anchor/latest/actions/list-browser-sessions?${params}`, {
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
      "page": 1,
      "sessions": [
        {
          "created_at": "string",
          "headless": true,
          "id": "string",
          "recording": true,
          "status": "string"
        }
      ],
      "total": 1,
      "total_pages": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `page` | number |  |
| `sessions[].created_at` | string |  |
| `sessions[].headless` | boolean |  |
| `sessions[].id` | string |  |
| `sessions[].recording` | boolean |  |
| `sessions[].status` | string |  |
| `total` | number |  |
| `total_pages` | number |  |

## Native endpoint

Through the native Anchor API, this operation is `GET /v1/sessions` (base URL `https://api.anchorbrowser.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-browser-sessions.md) for the provider-specific parameters and requirements.

