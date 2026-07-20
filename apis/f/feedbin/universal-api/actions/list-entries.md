# Feedbin: List Entries

Retrieves a list of entries from Feedbin.

```
GET https://connect.mindcloud.co/v1/universal/feedbin/latest/actions/list-entries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Feedbin `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/feedbin/latest/actions/list-entries?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/feedbin/latest/actions/list-entries?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `since` | date | no | Return entries created after this ISO 8601 timestamp. |
| `ids` | string | no | Comma-separated entry IDs. Feedbin allows up to 100 IDs per request. |
| `read` | boolean | no | Filter entries by read state. |
| `starred` | boolean | no | Filter entries by starred state. |
| `mode` | string | no | Use extended to include additional entry metadata. |
| `includeOriginal` | boolean | no | Include original entry data if the entry has been updated. |
| `includeEnclosure` | boolean | no | Include podcast/RSS enclosure data. |
| `includeContentDiff` | boolean | no | Include an HTML diff of changed content. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "author": "string",
      "content": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "extracted_content_url": "https://example.com",
      "feed_id": 1,
      "id": 1,
      "published": "2026-05-07T12:00:00.000Z",
      "summary": "string",
      "title": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `author` | string |  |
| `content` | string |  |
| `created_at` | date |  |
| `extracted_content_url` | string |  |
| `feed_id` | number |  |
| `id` | number |  |
| `published` | date |  |
| `summary` | string |  |
| `title` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Feedbin API, this operation is `GET entries.json` (base URL `https://api.feedbin.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-entries.md) for the provider-specific parameters and requirements.

