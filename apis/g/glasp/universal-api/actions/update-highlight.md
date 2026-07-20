# Glasp: Update Highlight

Updates an existing highlight in Glasp.

```
PUT https://connect.mindcloud.co/v1/universal/glasp/latest/actions/update-highlight
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Glasp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/glasp/latest/actions/update-highlight" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com",
  "highlightId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/glasp/latest/actions/update-highlight', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com",
    "highlightId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | Document URL that owns the highlight. |
| `highlightId` | string | yes | Identifier of the Glasp highlight to update. |
| `text` | string | no | Updated highlight text. |
| `note` | string | no | Updated note attached to the highlight. |
| `color` | string | no | Updated color for the highlight. |
| `location` | number | no | Updated highlight position within the document. |
| `highlightUrl` | string | no | Updated canonical URL for the highlight. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category": "string",
      "domain": "string",
      "glaspUrl": "https://example.com",
      "highlights": [
        [
          {}
        ]
      ],
      "id": "string",
      "title": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | string | Glasp content category for the document. |
| `domain` | string | Source domain for the document. |
| `glaspUrl` | string | Glasp URL for the saved document. |
| `highlights[]` | array<object> | Highlights returned for the updated document. |
| `highlights[].color` | string | Updated highlight color. |
| `highlights[].highlightUrl` | string | Unique highlight URL when Glasp provides one. |
| `highlights[].id` | string | Glasp highlight identifier. |
| `highlights[].location` | number | Updated highlight location or timestamp. |
| `highlights[].note` | string | Updated highlight note. |
| `highlights[].text` | string | Updated highlight text. |
| `highlights[].updatedAt` | date | When the highlight was last updated in Glasp. |
| `id` | string | Glasp document identifier containing the updated highlight. |
| `title` | string | Title of the source document. |
| `updatedAt` | date | When the document was last updated in Glasp. |
| `url` | string | Original source URL for the highlight. |

## Native endpoint

Through the native Glasp API, this operation is `PATCH /v1/highlights/update` (base URL `https://api.glasp.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-highlight.md) for the provider-specific parameters and requirements.

