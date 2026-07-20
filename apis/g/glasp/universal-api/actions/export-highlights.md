# Glasp: Export Highlights

Retrieves your Glasp highlights with optional filtering and pagination.

```
GET https://connect.mindcloud.co/v1/universal/glasp/latest/actions/export-highlights
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Glasp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/glasp/latest/actions/export-highlights?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/glasp/latest/actions/export-highlights?${params}`, {
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
| `pageCursor` | string | no | Pagination cursor returned from the previous Glasp export response. |
| `updatedAfter` | string | no | Only return highlights updated after this ISO date-time string. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "nextPageCursor": "string",
      "results": [
        [
          {}
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number | Number of exported Glasp documents in the current response page. |
| `nextPageCursor` | string | Cursor for the next export page when more results are available. |
| `results[]` | array<object> | Glasp documents returned by the export endpoint. |
| `results[].category` | string | Glasp content category for the document. |
| `results[].glaspUrl` | string | Glasp URL for the saved document. |
| `results[].highlights[]` | array<object> | Highlights nested under each exported document. |
| `results[].highlights[].color` | string | Highlight color. |
| `results[].highlights[].highlightUrl` | string | Unique URL for the highlight when Glasp provides one. |
| `results[].highlights[].id` | string | Glasp highlight identifier. |
| `results[].highlights[].note` | string | User note attached to the highlight. |
| `results[].highlights[].text` | string | Highlighted text content. |
| `results[].id` | string | Glasp document identifier. |
| `results[].title` | string | Title of the highlighted source document. |
| `results[].updatedAt` | date | When the document was last updated in Glasp. |
| `results[].url` | string | Original source URL. |

## Native endpoint

Through the native Glasp API, this operation is `GET /v1/highlights/export` (base URL `https://api.glasp.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/export-highlights.md) for the provider-specific parameters and requirements.

