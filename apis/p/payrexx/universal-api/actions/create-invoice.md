# Payrexx: Create Invoice

Creates an invoice in Payrexx.

```
POST https://connect.mindcloud.co/v1/universal/payrexx/latest/actions/create-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Payrexx `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/payrexx/latest/actions/create-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "language": "string",
  "currency": "string",
  "dueAfterDays": "5",
  "recipientCompany": "string",
  "recipientEmail": "ava@example.com",
  "recipientAddress": "string",
  "recipientZip": "string",
  "recipientCity": "string",
  "recipientCountry": "CH",
  "positionTitle": "string",
  "positionPrice": 1,
  "positionType": "piece",
  "positionNumber": "1",
  "positionVat": "0"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/payrexx/latest/actions/create-invoice', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "language": "string",
    "currency": "string",
    "dueAfterDays": "5",
    "recipientCompany": "string",
    "recipientEmail": "ava@example.com",
    "recipientAddress": "string",
    "recipientZip": "string",
    "recipientCity": "string",
    "recipientCountry": "CH",
    "positionTitle": "string",
    "positionPrice": 1,
    "positionType": "piece",
    "positionNumber": "1",
    "positionVat": "0"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `language` | string | yes | Invoice language ISO 639-1 code. |
| `currency` | string | yes | Invoice currency ISO 4217 code. |
| `dueAfterDays` | number | yes | Allowed invoice due period in days. Default: `5`. |
| `recipientCompany` | string | yes | Recipient company name. |
| `recipientEmail` | string | yes | Recipient email address. |
| `recipientAddress` | string | yes | Recipient street address. |
| `recipientZip` | string | yes | Recipient postal code. |
| `recipientCity` | string | yes | Recipient city. |
| `recipientCountry` | string | yes | Recipient country code (ISO 3166-1 alpha-2). Default: `CH`. |
| `positionTitle` | string | yes | Invoice line item title. |
| `positionPrice` | number | yes | Invoice line item price in the smallest currency unit. |
| `positionType` | string | yes | Invoice line item type. Default: `piece`. |
| `positionNumber` | number | yes | Invoice line item quantity/number. Default: `1`. |
| `positionVat` | number | yes | Invoice line item VAT percentage. Default: `0`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Payrexx API returns.

## Native endpoint

Through the native Payrexx API, this operation is `POST Bill/` (base URL `https://api.payrexx.com/v1.14/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-invoice.md) for the provider-specific parameters and requirements.

