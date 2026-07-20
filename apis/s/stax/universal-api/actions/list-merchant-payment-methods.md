# Stax: List Merchant Payment Methods

Retrieves merchant payment methods from Stax.

```
GET https://connect.mindcloud.co/v1/universal/stax/latest/actions/list-merchant-payment-methods
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stax `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stax/latest/actions/list-merchant-payment-methods?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stax/latest/actions/list-merchant-payment-methods?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "addressZip": "string",
      "cardExp": "string",
      "cardLastFour": "string",
      "cardType": "string",
      "customerId": "string",
      "id": "string",
      "isTokenized": true,
      "method": "string",
      "personName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addressZip` | string | Billing postal code. |
| `cardExp` | string | Card expiration in Stax format. |
| `cardLastFour` | string | Last four digits of the card. |
| `cardType` | string | Payment card brand. |
| `customerId` | string | Associated customer identifier. |
| `id` | string | Stax payment method identifier. |
| `isTokenized` | boolean | Whether the payment method is tokenized. |
| `method` | string | Payment method type. |
| `personName` | string | Cardholder or account holder name. |

## Native endpoint

Through the native Stax API, this operation is `GET /payment-method` (base URL `https://apiprod.fattlabs.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-merchant-payment-methods.md) for the provider-specific parameters and requirements.

