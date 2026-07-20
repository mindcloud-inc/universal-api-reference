# Anchor: List Session Downloads

Retrieves session downloads from Anchor.

```
GET https://connect.mindcloud.co/v1/universal/anchor/latest/actions/list-session-downloads
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Anchor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/anchor/latest/actions/list-session-downloads?connectionId=$CONNECTION_ID&sessionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sessionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/anchor/latest/actions/list-session-downloads?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sessionId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "items": [
        {
          "created_at": "string",
          "duration": 1,
          "file_link": "https://example.com",
          "id": "string",
          "origin_url": "https://example.com",
          "original_download_url": "https://example.com",
          "original_file_name": "Ava Chen",
          "size": 1,
          "suggested_file_name": "Ava Chen"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `items[].created_at` | string |  |
| `items[].duration` | number |  |
| `items[].file_link` | string |  |
| `items[].id` | string |  |
| `items[].origin_url` | string |  |
| `items[].original_download_url` | string |  |
| `items[].original_file_name` | string |  |
| `items[].size` | number |  |
| `items[].suggested_file_name` | string |  |

## Native endpoint

Through the native Anchor API, this operation is `GET /v1/sessions/:sessionId/downloads` (base URL `https://api.anchorbrowser.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-session-downloads.md) for the provider-specific parameters and requirements.

