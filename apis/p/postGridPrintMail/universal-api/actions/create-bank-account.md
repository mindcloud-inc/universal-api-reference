# PostGrid Print & Mail: Create Bank Account

Creates a bank account in PostGrid Print & Mail.

```
POST https://connect.mindcloud.co/v1/universal/postGridPrintMail/latest/actions/create-bank-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PostGrid Print & Mail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/postGridPrintMail/latest/actions/create-bank-account" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "bankName": "Ava Chen",
  "bankCountryCode": "string",
  "accountNumber": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/postGridPrintMail/latest/actions/create-bank-account', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "bankName": "Ava Chen",
    "bankCountryCode": "string",
    "accountNumber": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `bankName` | string | yes | The name of the bank. |
| `bankCountryCode` | string | yes | The bank country code. |
| `accountNumber` | string | yes | The bank account number. |
| `signatureText` | string | no | The signature text to print on cheques. |
| `signatureImage` | string | no | The signature image source to print on cheques. |
| `routingNumber` | string | no | The US routing number. |
| `transitNumber` | string | no | The Canadian transit number. |
| `routeNumber` | string | no | The Canadian route number. |
| `caDesignationNumber` | string | no | The Canadian designation number. |
| `bankPrimaryLine` | string | no | The primary address line for the bank. |
| `bankSecondaryLine` | string | no | The secondary address line for the bank. |
| `description` | string | no | An optional description visible in the API and dashboard. |
| `metadata` | object | no | Custom metadata for this bank account. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountNumberAndIDSHA256": "string",
      "accountNumberLast4": "string",
      "bankCountryCode": "string",
      "bankName": "Ava Chen",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": "string",
      "live": true,
      "object": "string",
      "routingNumber": "string",
      "signatureText": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountNumberAndIDSHA256` | string |  |
| `accountNumberLast4` | string |  |
| `bankCountryCode` | string |  |
| `bankName` | string |  |
| `createdAt` | date |  |
| `description` | string |  |
| `id` | string |  |
| `live` | boolean |  |
| `object` | string |  |
| `routingNumber` | string |  |
| `signatureText` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native PostGrid Print & Mail API, this operation is `POST /bank_accounts` (base URL `https://api.postgrid.com/print-mail/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-bank-account.md) for the provider-specific parameters and requirements.

