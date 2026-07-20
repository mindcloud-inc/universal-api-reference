# Readwise: Update Highlight

Updates an existing highlight in Readwise.

```
PUT https://connect.mindcloud.co/v1/universal/readwise/latest/actions/update-highlight
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Readwise `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/readwise/latest/actions/update-highlight" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "highlightId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/readwise/latest/actions/update-highlight', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "highlightId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `highlightId` | number | yes | The Readwise highlight ID to update. |
| `text` | string | no | The updated highlight text. |
| `note` | string | no | Annotation note attached to the specific highlight. |
| `color` | string | no | Highlight color tag. |
| `location` | string | no | Highlight location in the source text. |
| `url` | string | no | Unique URL of the specific highlight. |

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

Through the native Readwise API, this operation is `PATCH /api/v2/highlights/:highlightId/` (base URL `https://readwise.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-highlight.md) for the provider-specific parameters and requirements.

