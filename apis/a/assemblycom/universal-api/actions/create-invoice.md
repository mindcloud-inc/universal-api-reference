# Assembly.com: Create Invoice

Creates an invoice in Assembly.com.

```
POST https://connect.mindcloud.co/v1/universal/assemblycom/latest/actions/create-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Assembly.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/assemblycom/latest/actions/create-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "lineItems[].quantity": 1,
  "daysUntilDue": 1,
  "paymentMethodPreferences[]": [
    {}
  ],
  "paymentMethodPreferences[].type": "0",
  "paymentMethodPreferences[].feePaidByClient": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/assemblycom/latest/actions/create-invoice', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "lineItems[].quantity": 1,
    "daysUntilDue": 1,
    "paymentMethodPreferences[]": [{}],
    "paymentMethodPreferences[].type": "0",
    "paymentMethodPreferences[].feePaidByClient": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `clientId` | string | no | The ID of the client this invoice is assigned to. Leave empty if assigning to a company. |
| `companyId` | string | no | The ID of the company this invoice is assigned. This is required when an invoice is assigned to a company. |
| `templateId` | string | no | Unique ID of the invoice template to use. If provided, template values will be used for line items and invoice metadata. |
| `lineItems[]` | array<object> | no | Array of line items. Required if templateId is not provided. |
| `lineItems[].quantity` | number | yes | Quantity of the item (supports decimals). |
| `lineItems[].amount` | number | no | Amount in cents. Required if priceId not provided. |
| `lineItems[].priceId` | string | no | Unique ID of the price object. Required if amount is not provided. |
| `lineItems[].description` | string | no | Description of the item, ignored if priceId is provided. |
| `memo` | string | no | Memo attached to the invoice. |
| `daysUntilDue` | number | yes | The number of days from when the invoice is created until it is due. Max value is 30. |
| `taxPercentage` | number | no | Tax percentage to apply to the invoice amount. |
| `paymentMethodPreferences[]` | array<object> | yes | Array of preferences which specify which payment methods are allowed and how transaction fees are handled for each payment method. |
| `paymentMethodPreferences[].type` | string | yes | Payment method type. Values are creditCard or bankAccount. One of: `0`, `1`. |
| `paymentMethodPreferences[].feePaidByClient` | boolean | yes | When true, the transaction fee is paid by the client, otherwise it is covered by your account. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Assembly.com API returns.

## Native endpoint

Through the native Assembly.com API, this operation is `POST /invoices` (base URL `https://api.assembly.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-invoice.md) for the provider-specific parameters and requirements.

