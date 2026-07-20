# PostGrid Print & Mail: Create Cheque

Creates a cheque in PostGrid Print & Mail.

```
POST https://connect.mindcloud.co/v1/universal/postGridPrintMail/latest/actions/create-cheque
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PostGrid Print & Mail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/postGridPrintMail/latest/actions/create-cheque" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "to": "string",
  "from": "string",
  "bankAccount": "string",
  "amount": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/postGridPrintMail/latest/actions/create-cheque', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "to": "string",
    "from": "string",
    "bankAccount": "string",
    "amount": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `to` | string | yes | The recipient contact ID or recipient payload. |
| `from` | string | yes | The sender contact ID or sender payload. |
| `bankAccount` | string | yes | The PostGrid bank account ID to use for the cheque. |
| `amount` | number | yes | The cheque amount in the smallest currency unit. |
| `mergeVariables` | object | no | Template merge variables for the cheque. |
| `description` | string | no | An optional description visible in the API and dashboard. |
| `metadata` | object | no | Custom metadata for this cheque. |
| `sendDate` | date | no | Schedule the cheque for a future send date. |
| `mailingClass` | string | no | The mailing class for the cheque. |
| `memo` | string | no | The memo text for the cheque. |
| `message` | string | no | The message body for the cheque. |
| `logoURL` | string | no | A logo URL to print on the cheque. |
| `number` | number | no | The cheque number. |
| `envelope` | string | no | Envelope settings for the cheque. |
| `digitalOnly` | object | no | Digital delivery settings for the cheque. |
| `redirectTo` | string | no | A redirected recipient contact ID or payload. |
| `size` | string | no | The cheque paper size. |
| `currencyCode` | string | no | The currency code for the cheque amount. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "bankAccount": "string",
      "cancellation": {},
      "carrierTracking": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "currencyCode": "string",
      "description": "string",
      "envelope": "string",
      "from": {},
      "id": "string",
      "live": true,
      "mailingClass": "string",
      "number": 1,
      "object": "string",
      "pageCount": 1,
      "sendDate": "2026-05-07T12:00:00.000Z",
      "size": "string",
      "status": "string",
      "to": {},
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `bankAccount` | string |  |
| `cancellation` | object |  |
| `carrierTracking` | object |  |
| `createdAt` | date |  |
| `currencyCode` | string |  |
| `description` | string |  |
| `envelope` | string |  |
| `from` | object |  |
| `id` | string |  |
| `live` | boolean |  |
| `mailingClass` | string |  |
| `number` | number |  |
| `object` | string |  |
| `pageCount` | number |  |
| `sendDate` | date |  |
| `size` | string |  |
| `status` | string |  |
| `to` | object |  |
| `updatedAt` | date |  |
| `url` | string |  |

## Native endpoint

Through the native PostGrid Print & Mail API, this operation is `POST /cheques` (base URL `https://api.postgrid.com/print-mail/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-cheque.md) for the provider-specific parameters and requirements.

