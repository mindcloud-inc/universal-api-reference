# Crawlbase: Get Storage Item

Retrieves a stored page from Crawlbase.

```
GET https://connect.mindcloud.co/v1/universal/crawlbase/latest/actions/get-storage-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Crawlbase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/crawlbase/latest/actions/get-storage-item?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/crawlbase/latest/actions/get-storage-item?${params}`, {
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
| `rid` | string | no | Request identifier for the stored item. Provide either RID or URL. Example: `RID`. |
| `url` | string | no | Crawled URL for the stored item. Provide either URL or RID. Example: `https://example.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "body": "string",
      "original_status": 1,
      "pc_status": 1,
      "rid": "string",
      "stored_at": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `body` | string | Stored response body. |
| `original_status` | number | Original HTTP status. |
| `pc_status` | number | Crawlbase processing status. |
| `rid` | string | Storage request ID. |
| `stored_at` | date | Storage timestamp. |
| `url` | string | Stored URL. |

## Native endpoint

Through the native Crawlbase API, this operation is `GET /storage` (base URL `https://api.crawlbase.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-storage-item.md) for the provider-specific parameters and requirements.

