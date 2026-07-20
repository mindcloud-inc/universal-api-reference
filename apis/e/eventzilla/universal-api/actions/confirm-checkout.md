# Eventzilla: Confirm Checkout

Confirms a checkout in Eventzilla.

```
PUT https://connect.mindcloud.co/v1/universal/eventzilla/latest/actions/confirm-checkout
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eventzilla `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/eventzilla/latest/actions/confirm-checkout" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "eventId": 1,
  "eventDateId": 1,
  "checkoutId": 1,
  "paymentStatus": "string",
  "comments": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eventzilla/latest/actions/confirm-checkout', {
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
    "paymentStatus": "string",
    "comments": "string"
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
| `paymentStatus` | string | yes |  |
| `comments` | string | yes |  |
| `sendEmail` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "checkoutId": 1,
      "confirmationEmailSent": true,
      "currency": "string",
      "eventzillaFee": 1,
      "transactionDiscount": 1,
      "transactionRef": "string",
      "transactionStatus": "string",
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
| `confirmationEmailSent` | boolean |  |
| `currency` | string |  |
| `eventzillaFee` | number |  |
| `transactionDiscount` | number |  |
| `transactionRef` | string |  |
| `transactionStatus` | string |  |
| `transactionTax` | number |  |
| `transactionTotal` | number |  |

## Native endpoint

Through the native Eventzilla API, this operation is `POST /checkout/confirm` (base URL `https://www.eventzillaapi.net/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/confirm-checkout.md) for the provider-specific parameters and requirements.

