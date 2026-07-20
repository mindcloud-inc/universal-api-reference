# Assembly.com: Create Subscription

Creates a subscription in Assembly.com.

```
POST https://connect.mindcloud.co/v1/universal/assemblycom/latest/actions/create-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Assembly.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/assemblycom/latest/actions/create-subscription" \
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
  "paymentMethodPreferences[].feePaidByClient": true,
  "collectionMethod": "0"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/assemblycom/latest/actions/create-subscription', {
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
    "paymentMethodPreferences[].feePaidByClient": true,
    "collectionMethod": "0"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `clientId` | string | no | The ID of the client this subscription is assigned to. Leave empty if assigning to a company. |
| `companyId` | string | no | The ID of the company this subscription is assigned to. This is required when assigning to a company. |
| `templateId` | string | no | Unique ID of the invoice template to use. If provided, template values will be used for line items and invoice metadata. |
| `lineItems[]` | array<object> | no | Array of line items. Required if templateId is not provided. |
| `lineItems[].quantity` | number | yes | Quantity of the item (supports decimals). |
| `lineItems[].amount` | number | no | Amount in cents. Required if priceId is not provided. |
| `lineItems[].priceId` | string | no | Unique ID of the price object. Required if amount is not provided. |
| `lineItems[].description` | string | no | Description of the item, ignored if priceId is provided. |
| `memo` | string | no | Arbitrary string attached to the invoice, often used for display. |
| `daysUntilDue` | number | yes | The number of days from when the subscription invoice is created until it is due. Max value is 30. |
| `taxPercentage` | number | no | Tax percentage to apply to the invoice amount. |
| `interval` | string | no | Billing frequency. Required if line items do not include a recurring price. Values: day, week, month, quarterly, yearly. One of: `0`, `1`, `2`, `3`, `4`. |
| `intervalCount` | number | no | Number of intervals between billings. Default value is 1. Default: `1`. |
| `paymentMethodPreferences[]` | array<object> | yes | Array of preferences which specify which payment methods are allowed and how transaction fees are handled for each payment method. |
| `paymentMethodPreferences[].type` | string | yes | Payment method type. Values are creditCard or bankAccount. One of: `0`, `1`. |
| `paymentMethodPreferences[].feePaidByClient` | boolean | yes | When true, the transaction fee is paid by the client, otherwise it is covered by your account. |
| `collectionMethod` | string | yes | Specify how to charge for an invoice. Values: sendInvoice or chargeAutomatically. One of: `0`, `1`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Assembly.com API returns.

## Native endpoint

Through the native Assembly.com API, this operation is `POST /subscriptions` (base URL `https://api.assembly.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-subscription.md) for the provider-specific parameters and requirements.

