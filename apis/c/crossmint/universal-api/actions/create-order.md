# Crossmint: Create Order

Creates an order in Crossmint.

```
POST https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/create-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Crossmint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/create-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "payment.method": "base-sepolia",
  "payment.currency": "eth",
  "payment.receiptEmail": "buyer@example.com",
  "payment.payerAddress": "0x1234567890123456789012345678901234567890",
  "lineItems.collectionLocator": "string",
  "lineItems.callData.totalPrice": "0.0001",
  "recipient.email": "recipient@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/create-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "payment.method": "base-sepolia",
    "payment.currency": "eth",
    "payment.receiptEmail": "buyer@example.com",
    "payment.payerAddress": "0x1234567890123456789012345678901234567890",
    "lineItems.collectionLocator": "string",
    "lineItems.callData.totalPrice": "0.0001",
    "recipient.email": "recipient@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `payment.method` | string | yes | Blockchain or payment rail used to pay for the order. Default: `base-sepolia`. |
| `payment.currency` | string | yes | Currency used for payment. Default: `eth`. |
| `payment.receiptEmail` | string | yes | Email for the payment receipt. Example: `buyer@example.com`. |
| `payment.payerAddress` | string | yes | Wallet address that will pay for the order. Example: `0x1234567890123456789012345678901234567890`. |
| `lineItems.collectionLocator` | string | yes | Collection locator for the order line item. |
| `lineItems.callData.totalPrice` | string | yes | Quoted total price for the line item. Default: `0.0001`. |
| `recipient.email` | string | yes | Email for the NFT recipient. Example: `recipient@example.com`. |
| `locale` | string | no | Checkout locale. Default: `en-US`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Crossmint API returns.

## Native endpoint

Through the native Crossmint API, this operation is `POST /2022-06-09/orders` (base URL `https://staging.crossmint.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-order.md) for the provider-specific parameters and requirements.

