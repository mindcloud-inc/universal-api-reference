# Readwise: Get Highlight

Retrieves a highlight from the Readwise library.

```
GET https://connect.mindcloud.co/v1/universal/readwise/latest/actions/get-highlight
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Readwise `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/readwise/latest/actions/get-highlight?connectionId=$CONNECTION_ID&highlightId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "highlightId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/readwise/latest/actions/get-highlight?${params}`, {
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
| `highlightId` | number | yes | The unique id of the highlight to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bookId": 1,
      "color": "string",
      "createdAt": "string",
      "highlightedAt": "string",
      "id": 1,
      "location": 1,
      "locationType": "string",
      "note": "string",
      "readwiseUrl": "https://example.com",
      "text": "string",
      "updated": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bookId` | number |  |
| `color` | string |  |
| `createdAt` | string |  |
| `highlightedAt` | string |  |
| `id` | number |  |
| `location` | number |  |
| `locationType` | string |  |
| `note` | string |  |
| `readwiseUrl` | string |  |
| `text` | string |  |
| `updated` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Readwise API, this operation is `GET /api/v2/highlights/:highlight_id/` (base URL `https://readwise.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-highlight.md) for the provider-specific parameters and requirements.

