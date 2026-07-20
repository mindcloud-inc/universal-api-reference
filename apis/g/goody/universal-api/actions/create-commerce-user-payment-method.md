# Goody: Create Commerce User Payment Method

Creates a commerce user payment method in Goody.

```
POST https://connect.mindcloud.co/v1/universal/goody/latest/actions/create-commerce-user-payment-method
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Goody `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/goody/latest/actions/create-commerce-user-payment-method" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "cardholderName": "Ava Chen",
  "commerceEndUserId": "string",
  "interimCardKey": "string",
  "billingAddress": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/goody/latest/actions/create-commerce-user-payment-method', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "cardholderName": "Ava Chen",
    "commerceEndUserId": "string",
    "interimCardKey": "string",
    "billingAddress": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cardholderName` | string | yes | The name on the card. |
| `commerceEndUserId` | string | yes | The user ID in your app to associate this payment method with. |
| `interimCardKey` | string | yes | The temporary card token returned by Goody’s embedded payment form. |
| `billingAddress` | object | yes | Billing address object. Goody’s example includes `address_1`, `address_2`, `city`, `state`, `postal_code`, and `country`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "card_brand": "string",
      "card_exp_month": 1,
      "card_exp_year": 1,
      "card_last_4": "string",
      "cardholder_name": "Ava Chen",
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `card_brand` | string |  |
| `card_exp_month` | number |  |
| `card_exp_year` | number |  |
| `card_last_4` | string |  |
| `cardholder_name` | string |  |
| `created_at` | date |  |
| `id` | string |  |

## Native endpoint

Through the native Goody API, this operation is `POST /v1/commerce_user_payment_methods` (base URL `https://api.ongoody.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-commerce-user-payment-method.md) for the provider-specific parameters and requirements.

