# Stax: List Customer Payment Methods

Retrieves a customer's payment methods from Stax.

```
GET https://connect.mindcloud.co/v1/universal/stax/latest/actions/list-customer-payment-methods
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stax `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stax/latest/actions/list-customer-payment-methods?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stax/latest/actions/list-customer-payment-methods?${params}`, {
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
| `customerId` | string | no | Customer identifier |

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

Through the native Stax API, this operation is `GET /customer/:customerId/payment-method` (base URL `https://apiprod.fattlabs.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-customer-payment-methods.md) for the provider-specific parameters and requirements.

