# Rillion Prime: Calculate Vat Account Coding For Invoice



```
PUT https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/calculate-vat-account-coding-for-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rillion Prime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/calculate-vat-account-coding-for-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "invoiceId": 1,
  "role": "Administrator",
  "invoiceAccountCoding": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/calculate-vat-account-coding-for-invoice', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "invoiceId": 1,
    "role": "Administrator",
    "invoiceAccountCoding": ["string"],
    "invoiceAccountCoding": ["string"],
    "invoiceAccountCoding": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `invoiceId` | number | yes | Path value for InvoiceId. |
| `role` | string | yes | Path value for Role. Example: `Administrator`. |
| `saveAccountCoding` | boolean | no | Optional query value for SaveAccountCoding. |
| `invoiceAccountCoding` | array | yes | Request body value for InvoiceAccountCoding. |
| `invoiceAccountCoding` | array | yes | Request body value for InvoiceAccountCoding. |
| `invoiceAccountCoding` | array | yes | Request body value for InvoiceAccountCoding. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Rillion Prime API returns.

## Native endpoint

Through the native Rillion Prime API, this operation is `POST /invoice/:invoiceId/CalculateVat/role/:role` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/calculate-vat-account-coding-for-invoice.md) for the provider-specific parameters and requirements.

