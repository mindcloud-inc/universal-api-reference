# Print.one Postcards: Update Batch

Updates an existing batch in Print.one Postcards.

```
PUT https://connect.mindcloud.co/v1/universal/printonePostcards/latest/actions/update-batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Print.one Postcards `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/printonePostcards/latest/actions/update-batch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "batchId": "string",
  "ready": "true",
  "requiredCount": "301"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/printonePostcards/latest/actions/update-batch', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "batchId": "string",
    "ready": "true",
    "requiredCount": "301"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `batchId` | string | yes | Batch ID to update |
| `ready` | string | no | When true, send the batch as soon as requirements are met |
| `ready` | boolean | yes | When true, send the batch as soon as requirements are met Default: `true`. |
| `requiredCount` | number | yes | Minimum number of orders required before the batch is sent Default: `301`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archivedAt": "2026-05-07T12:00:00.000Z",
      "billingId": "string",
      "companyId": "string",
      "countryId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "expectedDeliveryTimeframe": [
        "2026-05-07T12:00:00.000Z"
      ],
      "finish": "string",
      "format": "string",
      "id": "string",
      "isBillable": true,
      "name": "Ava Chen",
      "orders": {},
      "requiredCount": 1,
      "sendDate": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "templateId": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archivedAt` | date |  |
| `billingId` | string |  |
| `companyId` | string |  |
| `countryId` | string |  |
| `createdAt` | date |  |
| `expectedDeliveryTimeframe` | array<date> |  |
| `finish` | string |  |
| `format` | string |  |
| `id` | string |  |
| `isBillable` | boolean |  |
| `name` | string |  |
| `orders` | object |  |
| `requiredCount` | number |  |
| `sendDate` | date |  |
| `status` | string |  |
| `templateId` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Print.one Postcards API, this operation is `PATCH /v2/batches/:batchId` (base URL `https://api.print.one`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-batch.md) for the provider-specific parameters and requirements.

