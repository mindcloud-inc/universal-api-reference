# Vouchery.io: Create Redemption



```
POST https://connect.mindcloud.co/v1/universal/voucheryio/latest/actions/create-redemption
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vouchery.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/voucheryio/latest/actions/create-redemption" \
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
const response = await fetch('https://connect.mindcloud.co/v1/universal/voucheryio/latest/actions/create-redemption', {
  method: 'POST',
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
| `code` | string | yes | Voucher code from the path. |
| `additionalCategories` | object | yes | Additional redemption categories object. |
| `confirmed` | boolean | yes | Whether the redemption is confirmed immediately. |
| `productItems[]` | array<object> | no | Purchased product items. |
| `customerIdentifier` | string | no | Customer identifier in your system. |
| `shippingCost` | number | no | Shipping cost. |
| `totalTransactionCost` | number | no | Total transaction cost excluding shipping. |
| `transactionId` | string | no | Underlying transaction identifier. |
| `userAgent` | string | no | User agent string. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Vouchery.io API returns.

## Native endpoint

Through the native Vouchery.io API, this operation is `POST /vouchers/:code/redemptions` (base URL `https://mindcloud.sandbox.vouchery.app/api/v2.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-redemption.md) for the provider-specific parameters and requirements.

