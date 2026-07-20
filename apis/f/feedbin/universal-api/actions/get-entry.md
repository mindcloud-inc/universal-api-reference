# Feedbin: Get Entry

Retrieves a single entry from Feedbin.

```
GET https://connect.mindcloud.co/v1/universal/feedbin/latest/actions/get-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Feedbin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/feedbin/latest/actions/get-entry?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/feedbin/latest/actions/get-entry?${params}`, {
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
| `id` | number | yes | Feedbin entry ID. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
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

Through the native Feedbin API, this operation is `GET entries/[:id].json` (base URL `https://api.feedbin.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-entry.md) for the provider-specific parameters and requirements.

