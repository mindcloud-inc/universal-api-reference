# Print.one Postcards: Create Order

Creates a new order in Print.one Postcards.

```
POST https://connect.mindcloud.co/v1/universal/printonePostcards/latest/actions/create-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Print.one Postcards `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/printonePostcards/latest/actions/create-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templateId": "string",
  "finish": "GLOSSY",
  "mergeVariables": {},
  "recipient.name": "Ava Chen",
  "recipient.address": "string",
  "recipient.postalCode": "string",
  "recipient.city": "string",
  "recipient.country": "NL"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/printonePostcards/latest/actions/create-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "templateId": "string",
    "finish": "GLOSSY",
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
| `templateId` | string | yes | Template ID for the order |
| `finish` | string | yes | Finish of the postcard Default: `GLOSSY`. |
| `mergeVariables` | object | yes | Personalization data as a JSON object Default: `{}`. |
| `recipient.name` | string | yes | Recipient name |
| `recipient.address` | string | yes | Recipient street address |
| `recipient.postalCode` | string | yes | Recipient postal code |
| `recipient.city` | string | yes | Recipient city |
| `recipient.country` | string | yes | Recipient country ISO code Default: `NL`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "anonymizedAt": "2026-05-07T12:00:00.000Z",
      "auditLogs": [
        {}
      ],
      "companyId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "csvOrderId": "string",
      "definitiveCountryId": "string",
      "deliverySpeed": "string",
      "errors": [
        "string"
      ],
      "finish": "string",
      "format": "string",
      "friendlyStatus": "string",
      "id": "string",
      "isBillable": true,
      "mergeVariables": {},
      "metadata": {},
      "recipient": {},
      "region": "string",
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
| `anonymizedAt` | date |  |
| `auditLogs` | array<object> |  |
| `companyId` | string |  |
| `createdAt` | date |  |
| `csvOrderId` | string |  |
| `definitiveCountryId` | string |  |
| `deliverySpeed` | string |  |
| `errors` | array<string> |  |
| `finish` | string |  |
| `format` | string |  |
| `friendlyStatus` | string |  |
| `id` | string |  |
| `isBillable` | boolean |  |
| `mergeVariables` | object |  |
| `metadata` | object |  |
| `recipient` | object |  |
| `region` | string |  |
| `sendDate` | date |  |
| `sender` | object |  |
| `status` | string |  |
| `templateId` | string |  |
| `templateVersion` | number |  |
| `updatedAt` | date |  |
| `warnings` | array<string> |  |

## Native endpoint

Through the native Print.one Postcards API, this operation is `POST /v2/orders` (base URL `https://api.print.one`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-order.md) for the provider-specific parameters and requirements.

