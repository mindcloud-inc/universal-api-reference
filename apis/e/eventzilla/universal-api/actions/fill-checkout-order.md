# Eventzilla: Fill Checkout Order

Updates checkout order details in Eventzilla.

```
PUT https://connect.mindcloud.co/v1/universal/eventzilla/latest/actions/fill-checkout-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eventzilla `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/eventzilla/latest/actions/fill-checkout-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "eventId": 1,
  "eventDateId": 1,
  "checkoutId": 1,
  "buyerDetails[]": [
    {}
  ],
  "tickets[]": [
    {}
  ],
  "paymentId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eventzilla/latest/actions/fill-checkout-order', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "eventId": 1,
    "eventDateId": 1,
    "checkoutId": 1,
    "buyerDetails[]": [{}],
    "tickets[]": [{}],
    "paymentId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `eventId` | number | yes |  |
| `eventDateId` | number | yes |  |
| `checkoutId` | number | yes |  |
| `buyerDetails[]` | array<object> | yes |  |
| `tickets[]` | array<object> | yes |  |
| `paymentId` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "checkoutId": 1,
      "currency": "string",
      "eventzillaFee": 1,
      "transactionDiscount": 1,
      "transactionRef": "string",
      "transactionTax": 1,
      "transactionTotal": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `checkoutId` | number |  |
| `currency` | string |  |
| `eventzillaFee` | number |  |
| `transactionDiscount` | number |  |
| `transactionRef` | string |  |
| `transactionTax` | number |  |
| `transactionTotal` | number |  |

## Native endpoint

Through the native Eventzilla API, this operation is `POST /checkout/fillorder` (base URL `https://www.eventzillaapi.net/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fill-checkout-order.md) for the provider-specific parameters and requirements.

