# Print.one Postcards: Get Batch Stats

Retrieves batch statistics from Print.one Postcards.

```
GET https://connect.mindcloud.co/v1/universal/printonePostcards/latest/actions/get-batch-stats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Print.one Postcards `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/printonePostcards/latest/actions/get-batch-stats?connectionId=$CONNECTION_ID&batchId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "batchId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/printonePostcards/latest/actions/get-batch-stats?${params}`, {
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
| `batchId` | string | yes | Batch ID to inspect |

## Response

```json
{
  "success": true,
  "data": [
    {
      "totalOrders": 1,
      "totalPurchases": 1,
      "totalRevenue": 1,
      "totalScans": 1,
      "uniqueScans": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `totalOrders` | number |  |
| `totalPurchases` | number |  |
| `totalRevenue` | number |  |
| `totalScans` | number |  |
| `uniqueScans` | number |  |

## Native endpoint

Through the native Print.one Postcards API, this operation is `GET /v2/batches/:batchId/stats` (base URL `https://api.print.one`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-batch-stats.md) for the provider-specific parameters and requirements.

