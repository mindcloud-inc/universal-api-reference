# Print.one Postcards: Add Orders To Batch

Adds orders to a batch in Print.one Postcards.

```
POST https://connect.mindcloud.co/v1/universal/printonePostcards/latest/actions/add-orders-to-batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Print.one Postcards `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/printonePostcards/latest/actions/add-orders-to-batch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "batchId": "string",
  "mergeVariables": {},
  "recipient.name": "Ava Chen",
  "recipient.address": "string",
  "recipient.postalCode": "string",
  "recipient.city": "string",
  "recipient.country": "NL"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/printonePostcards/latest/actions/add-orders-to-batch', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "batchId": "string",
    "mergeVariables": {},
    "recipient.name": "Ava Chen",
    "recipient.address": "string",
    "recipient.postalCode": "string",
    "recipient.city": "string",
    "recipient.country": "NL"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `batchId` | string | yes | Batch ID to add orders to |
| `mergeVariables` | object | yes | Personalization data as a JSON object Default: `{}`. |
| `recipient.name` | string | yes | Recipient name |
| `recipient.address` | string | yes | Recipient street address |
| `recipient.postalCode` | string | yes | Recipient postal code |
| `recipient.city` | string | yes | Recipient city |
| `recipient.country` | string | yes | Recipient country ISO code Default: `NL`. |
| `autoGenNextBatch` | boolean | no | Generate a new batch automatically when this one no longer accepts orders Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "batchId": "string",
      "companyId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "csvOrderId": "string",
      "errors": [
        "string"
      ],
      "finish": "string",
      "format": "string",
      "friendlyStatus": "string",
      "id": "string",
      "mergeVariables": {},
      "metadata": {},
      "recipient": {},
      "sendDate": "2026-05-07T12:00:00.000Z",
      "sender": {},
      "status": "string",
      "templateId": "string",
      "templateVersion": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "warnings": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `batchId` | string |  |
| `companyId` | string |  |
| `createdAt` | date |  |
| `csvOrderId` | string |  |
| `errors` | array<string> |  |
| `finish` | string |  |
| `format` | string |  |
| `friendlyStatus` | string |  |
| `id` | string |  |
| `mergeVariables` | object |  |
| `metadata` | object |  |
| `recipient` | object |  |
| `sendDate` | date |  |
| `sender` | object |  |
| `status` | string |  |
| `templateId` | string |  |
| `templateVersion` | number |  |
| `updatedAt` | date |  |
| `warnings` | array<string> |  |

## Native endpoint

Through the native Print.one Postcards API, this operation is `POST /v2/batches/:batchId/orders` (base URL `https://api.print.one`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-orders-to-batch.md) for the provider-specific parameters and requirements.

