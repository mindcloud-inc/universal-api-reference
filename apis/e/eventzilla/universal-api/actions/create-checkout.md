# Eventzilla: Create Checkout

Creates a checkout in Eventzilla.

```
POST https://connect.mindcloud.co/v1/universal/eventzilla/latest/actions/create-checkout
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eventzilla `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eventzilla/latest/actions/create-checkout" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "eventId": 1,
  "eventDateId": 1,
  "ticketTypes[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eventzilla/latest/actions/create-checkout', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "eventId": 1,
    "eventDateId": 1,
    "ticketTypes[]": [{}]
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
| `ticketTypes[]` | array<object> | yes |  |
| `discountCode` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "checkoutId": 1,
      "currency": "string",
      "eventzillaFee": 1,
      "tickets": [
        {}
      ],
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
| `tickets` | array<object> |  |
| `transactionDiscount` | number |  |
| `transactionRef` | string |  |
| `transactionTax` | number |  |
| `transactionTotal` | number |  |

## Native endpoint

Through the native Eventzilla API, this operation is `POST /checkout/create` (base URL `https://www.eventzillaapi.net/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-checkout.md) for the provider-specific parameters and requirements.

