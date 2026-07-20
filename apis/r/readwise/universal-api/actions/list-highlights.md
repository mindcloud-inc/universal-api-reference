# Readwise: List Highlights

Retrieves highlights from the Readwise library.

```
GET https://connect.mindcloud.co/v1/universal/readwise/latest/actions/list-highlights
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Readwise `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/readwise/latest/actions/list-highlights?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/readwise/latest/actions/list-highlights?${params}`, {
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
| `bookId` | number | no | Return highlights for a specific book. |
| `updatedLt` | string | no | Return highlights updated before this ISO 8601 datetime. |
| `updatedGt` | string | no | Return highlights updated after this ISO 8601 datetime. |
| `highlightedAtLt` | string | no | Return highlights taken before this ISO 8601 datetime. |
| `highlightedAtGt` | string | no | Return highlights taken after this ISO 8601 datetime. |

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

Through the native Readwise API, this operation is `GET /api/v2/highlights/` (base URL `https://readwise.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-highlights.md) for the provider-specific parameters and requirements.

