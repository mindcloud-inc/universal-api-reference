# Crawlbase: Get Storage Total Count

Retrieves the total storage item count from Crawlbase.

```
GET https://connect.mindcloud.co/v1/universal/crawlbase/latest/actions/get-storage-total-count
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Crawlbase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/crawlbase/latest/actions/get-storage-total-count?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/crawlbase/latest/actions/get-storage-total-count?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "totalCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `totalCount` | number | Total number of documents in Crawlbase storage. |

## Native endpoint

Through the native Crawlbase API, this operation is `GET /storage/total_count` (base URL `https://api.crawlbase.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-storage-total-count.md) for the provider-specific parameters and requirements.

