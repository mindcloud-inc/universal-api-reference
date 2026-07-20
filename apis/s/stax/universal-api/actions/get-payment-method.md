# Stax: Get Payment Method

Retrieves a payment method from Stax.

```
GET https://connect.mindcloud.co/v1/universal/stax/latest/actions/get-payment-method
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stax `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stax/latest/actions/get-payment-method?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stax/latest/actions/get-payment-method?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | no | Payment method identifier |

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
      "createdAt": "string",
      "customerId": "string",
      "id": "string",
      "isDefault": true,
      "isTokenized": true,
      "method": "string",
      "personName": "Ava Chen",
      "updatedAt": "string"
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
| `createdAt` | string | Creation timestamp. |
| `customerId` | string | Associated customer identifier. |
| `id` | string | Stax payment method identifier. |
| `isDefault` | boolean | Whether the payment method is the default. |
| `isTokenized` | boolean | Whether the payment method is tokenized. |
| `method` | string | Payment method type. |
| `personName` | string | Cardholder or account holder name. |
| `updatedAt` | string | Last update timestamp. |

## Native endpoint

Through the native Stax API, this operation is `GET /payment-method/:id` (base URL `https://apiprod.fattlabs.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-payment-method.md) for the provider-specific parameters and requirements.

