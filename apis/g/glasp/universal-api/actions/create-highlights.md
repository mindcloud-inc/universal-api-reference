# Glasp: Create Highlights

Creates new highlights in your Glasp account.

```
POST https://connect.mindcloud.co/v1/universal/glasp/latest/actions/create-highlights
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Glasp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/glasp/latest/actions/create-highlights" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "highlights[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/glasp/latest/actions/create-highlights', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "highlights[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `highlights[]` | array<object> | yes | Array of Glasp highlight objects to create. Each object should include at least title, url, and text. |

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
| `highlights[]` | array<object> | Highlights created under the document. |
| `highlights[].color` | string | Created highlight color. |
| `highlights[].highlightedAt` | date | When the highlight was recorded in Glasp. |
| `highlights[].highlightUrl` | string | Unique highlight URL when Glasp provides one. |
| `highlights[].id` | string | Glasp highlight identifier. |
| `highlights[].location` | number | Optional highlight location or timestamp. |
| `highlights[].note` | string | Created highlight note. |
| `highlights[].text` | string | Created highlight text. |
| `id` | string | Glasp document identifier created or reused for the imported highlights. |
| `title` | string | Title of the source document. |
| `updatedAt` | date | When the document was last updated in Glasp. |
| `url` | string | Original source URL for the created highlights. |

## Native endpoint

Through the native Glasp API, this operation is `POST /v1/highlights/create` (base URL `https://api.glasp.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-highlights.md) for the provider-specific parameters and requirements.

