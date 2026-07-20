# Readwise: Export Highlights

Retrieves books and highlights from Readwise.

```
GET https://connect.mindcloud.co/v1/universal/readwise/latest/actions/export-highlights
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Readwise `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/readwise/latest/actions/export-highlights?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/readwise/latest/actions/export-highlights?${params}`, {
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
| `updatedAfter` | date | no | Fetch only highlights updated after this ISO 8601 timestamp. |
| `ids` | string | no | Comma-separated list of Readwise user book IDs to export. |
| `includeDeleted` | boolean | no | Whether to include deleted highlights for sync use cases. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `pageCursor` | string | no | Cursor returned by a previous export request to continue fetching books and highlights. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "author": "string",
      "bookTags": [
        {}
      ],
      "coverImageUrl": "https://example.com",
      "highlights": [
        {}
      ],
      "readableTitle": "string",
      "source": "string",
      "title": "string",
      "uniqueUrl": "https://example.com",
      "userBookId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `author` | string |  |
| `bookTags[]` | object |  |
| `coverImageUrl` | string |  |
| `highlights[]` | object |  |
| `readableTitle` | string |  |
| `source` | string |  |
| `title` | string |  |
| `uniqueUrl` | string |  |
| `userBookId` | number |  |

## Native endpoint

Through the native Readwise API, this operation is `GET /api/v2/export/` (base URL `https://readwise.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/export-highlights.md) for the provider-specific parameters and requirements.

