# Print.one Postcards: Get Batch CSV Import Details

Retrieves batch CSV import details from Print.one Postcards.

```
GET https://connect.mindcloud.co/v1/universal/printonePostcards/latest/actions/get-batch-csv-import-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Print.one Postcards `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/printonePostcards/latest/actions/get-batch-csv-import-details?connectionId=$CONNECTION_ID&batchId=string&csvId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "batchId": "string",
  "csvId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/printonePostcards/latest/actions/get-batch-csv-import-details?${params}`, {
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
| `batchId` | string | yes | The batch ID. |
| `csvId` | string | yes | The CSV import ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "batchId": "string",
      "cancelledOrderCount": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "estimatedOrderCount": 1,
      "failedOrderCount": 1,
      "friendlyStatus": "string",
      "id": "string",
      "isBillable": true,
      "mapping": {},
      "processedOrderCount": 1,
      "sendDate": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "totalOrderCount": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `batchId` | string |  |
| `cancelledOrderCount` | number |  |
| `createdAt` | date |  |
| `estimatedOrderCount` | number |  |
| `failedOrderCount` | number |  |
| `friendlyStatus` | string |  |
| `id` | string |  |
| `isBillable` | boolean |  |
| `mapping` | object |  |
| `processedOrderCount` | number |  |
| `sendDate` | date |  |
| `status` | string |  |
| `totalOrderCount` | number |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Print.one Postcards API, this operation is `GET /v2/batches/:batchId/orders/csv/:csvId` (base URL `https://api.print.one`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-batch-csv-import-details.md) for the provider-specific parameters and requirements.

