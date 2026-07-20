# Print.one Postcards: Create Batch

Creates a new batch in Print.one Postcards.

```
POST https://connect.mindcloud.co/v1/universal/printonePostcards/latest/actions/create-batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Print.one Postcards `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/printonePostcards/latest/actions/create-batch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "templateId": "string",
  "finish": "GLOSSY",
  "ready": "true",
  "requiredCount": "1"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/printonePostcards/latest/actions/create-batch', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "templateId": "string",
    "finish": "GLOSSY",
    "ready": "true",
    "requiredCount": "1"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Name of the batch |
| `templateId` | string | yes | Template ID every order in the batch will use |
| `finish` | string | yes | Finish every order in the batch will use Default: `GLOSSY`. |
| `ready` | boolean | yes | When true, send the batch as soon as requirements are met Default: `true`. |
| `requiredCount` | number | yes | Minimum number of orders required before the batch is sent Default: `1`. |

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

Through the native Print.one Postcards API, this operation is `POST /v2/batches` (base URL `https://api.print.one`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-batch.md) for the provider-specific parameters and requirements.

