# Vouchery.io: Validate Voucher



```
PUT https://connect.mindcloud.co/v1/universal/voucheryio/latest/actions/validate-voucher
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vouchery.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/voucheryio/latest/actions/validate-voucher" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "code": "string",
  "additionalCategories": {},
  "confirmed": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/voucheryio/latest/actions/validate-voucher', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "code": "string",
    "additionalCategories": {},
    "confirmed": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `code` | string | yes | Voucher code |
| `additionalCategories` | object | yes | Additional categories |
| `confirmed` | boolean | yes | Whether the redemption is confirmed |
| `productItems[]` | array<object> | no | Product items |
| `customerIdentifier` | string | no | Customer identifier |
| `shippingCost` | number | no | Shipping cost |
| `totalTransactionCost` | number | no | Total transaction cost |
| `transactionId` | string | no | Transaction ID |
| `userAgent` | string | no | User agent |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Vouchery.io API returns.

## Native endpoint

Through the native Vouchery.io API, this operation is `PUT /vouchers/:code/validate` (base URL `https://mindcloud.sandbox.vouchery.app/api/v2.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-voucher.md) for the provider-specific parameters and requirements.

