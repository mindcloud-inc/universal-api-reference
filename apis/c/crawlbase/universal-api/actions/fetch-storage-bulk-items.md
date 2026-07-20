# Crawlbase: Fetch Storage Bulk Items

Retrieves stored pages in bulk from Crawlbase.

```
GET https://connect.mindcloud.co/v1/universal/crawlbase/latest/actions/fetch-storage-bulk-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Crawlbase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/crawlbase/latest/actions/fetch-storage-bulk-items?connectionId=$CONNECTION_ID&rids=RID1%2CRID2%2CRID3" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "rids": "RID1,RID2,RID3"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/crawlbase/latest/actions/fetch-storage-bulk-items?${params}`, {
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
| `rids` | string<string> | yes | Array of storage RIDs to retrieve. Crawlbase processes a maximum of 100 RIDs per request. Accepts multiple values as an array. Example: `RID1,RID2,RID3`. |
| `autoDelete` | boolean | no | Whether Crawlbase should delete fetched storage items after retrieval. Defaults to false. Default: `false`. |

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
| `body` | string | Base64 encoded and gzip compressed stored content. |
| `original_status` | number | Original HTTP status. |
| `pc_status` | number | Crawlbase processing status. |
| `rid` | string | Storage request ID. |
| `stored_at` | date | Storage timestamp. |
| `url` | string | Stored URL. |

## Native endpoint

Through the native Crawlbase API, this operation is `POST /storage/bulk` (base URL `https://api.crawlbase.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fetch-storage-bulk-items.md) for the provider-specific parameters and requirements.

