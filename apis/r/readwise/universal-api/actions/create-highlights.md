# Readwise: Create Highlights

Creates new highlights in the Readwise library.

```
POST https://connect.mindcloud.co/v1/universal/readwise/latest/actions/create-highlights
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Readwise `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/readwise/latest/actions/create-highlights" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "highlights[]": [
    {}
  ],
  "highlights[].text": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/readwise/latest/actions/create-highlights', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "highlights[]": [{}],
    "highlights[].text": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `highlights[]` | array<object> | yes | Array of highlight objects to create or update. |
| `highlights[].text` | string | yes | The highlight text. |
| `highlights[].title` | string | no | Title of the source book, article, or podcast. |
| `highlights[].author` | string | no | Author of the source book, article, or podcast. |
| `highlights[].image_url` | string | no | Cover image URL for the source. |
| `highlights[].source_url` | string | no | URL of the source article or podcast. |
| `highlights[].source_type` | string | no | A meaningful unique identifier for your app. |
| `highlights[].category` | string | no | Category for the highlight source. |
| `highlights[].note` | string | no | Annotation note attached to the highlight. |
| `highlights[].location` | number | no | Highlight location in the source text. |
| `highlights[].location_type` | string | no | How the highlight location should be interpreted. |
| `highlights[].highlighted_at` | string | no | ISO 8601 datetime when the highlight was taken. |
| `highlights[].highlight_url` | string | no | Unique URL of the specific highlight. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "author": "string",
      "category": "string",
      "coverImageUrl": "https://example.com",
      "documentNote": "string",
      "highlightsUrl": "https://example.com",
      "id": 1,
      "lastHighlightAt": "string",
      "numHighlights": 1,
      "source": "string",
      "sourceUrl": "https://example.com",
      "title": "string",
      "updated": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `author` | string |  |
| `category` | string |  |
| `coverImageUrl` | string |  |
| `documentNote` | string |  |
| `highlightsUrl` | string |  |
| `id` | number |  |
| `lastHighlightAt` | string |  |
| `numHighlights` | number |  |
| `source` | string |  |
| `sourceUrl` | string |  |
| `title` | string |  |
| `updated` | string |  |

## Native endpoint

Through the native Readwise API, this operation is `POST /api/v2/highlights/` (base URL `https://readwise.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-highlights.md) for the provider-specific parameters and requirements.

