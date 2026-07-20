# Olostep: List Batch Items

Retrieves items from an Olostep batch.

```
GET https://connect.mindcloud.co/v1/universal/olostep/latest/actions/list-batch-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Olostep `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/olostep/latest/actions/list-batch-items?connectionId=$CONNECTION_ID&limit=25&offset=0&batchId=batch_123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "batchId": "batch_123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/olostep/latest/actions/list-batch-items?${params}`, {
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
| `batchId` | string | yes | The ID of the batch whose items you want to list. Example: `batch_123`. |
| `status` | string | no | Optional item status to retrieve from the batch. One of: `0`, `1`. Example: `completed`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "items": [
        {
          "customId": "string",
          "retrieveId": "string",
          "url": "https://example.com"
        }
      ],
      "itemsCount": 1,
      "object": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `items[].customId` | string |  |
| `items[].retrieveId` | string |  |
| `items[].url` | string |  |
| `itemsCount` | number |  |
| `object` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Olostep API, this operation is `GET /v1/batches/[:batch_id]/items` (base URL `https://api.olostep.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-batch-items.md) for the provider-specific parameters and requirements.

