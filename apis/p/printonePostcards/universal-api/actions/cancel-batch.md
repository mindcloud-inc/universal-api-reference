# Print.one Postcards: Cancel Batch

Cancels an existing batch in Print.one Postcards.

```
DELETE https://connect.mindcloud.co/v1/universal/printonePostcards/latest/actions/cancel-batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Print.one Postcards `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/printonePostcards/latest/actions/cancel-batch?connectionId=$CONNECTION_ID&batchId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "batchId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/printonePostcards/latest/actions/cancel-batch?${params}`, {
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

Through the native Print.one Postcards API, this operation is `POST /v2/batches/:batchId/cancel` (base URL `https://api.print.one`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-batch.md) for the provider-specific parameters and requirements.

