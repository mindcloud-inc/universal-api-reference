# Crawlbase: List Storage RIDs

Retrieves storage record IDs from Crawlbase.

```
GET https://connect.mindcloud.co/v1/universal/crawlbase/latest/actions/list-storage-rids
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Crawlbase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/crawlbase/latest/actions/list-storage-rids?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/crawlbase/latest/actions/list-storage-rids?${params}`, {
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
| `limit` | number | no | Maximum number of storage RIDs to return. |
| `scroll` | boolean | no | Use Crawlbase scroll mode for paginated RID retrieval. |
| `scrollId` | string | no | Scroll identifier returned by a previous storage RIDs request. |
| `scrollOrder` | list | no | RID scroll order. One of: `0`, `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "rids": [
        "string"
      ],
      "scroll_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `rids` | array<string> | Stored request IDs. |
| `scroll_id` | string | Scroll identifier for pagination when provided by Crawlbase. |

## Native endpoint

Through the native Crawlbase API, this operation is `GET /storage/rids` (base URL `https://api.crawlbase.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-storage-rids.md) for the provider-specific parameters and requirements.

