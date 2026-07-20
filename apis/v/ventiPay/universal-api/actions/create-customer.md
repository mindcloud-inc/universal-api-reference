# VentiPay: Create Customer

Creates a new customer in VentiPay.

```
POST https://connect.mindcloud.co/v1/universal/ventiPay/latest/actions/create-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a VentiPay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ventiPay/latest/actions/create-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "country": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ventiPay/latest/actions/create-customer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "country": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | Email del cliente. |
| `country` | string | yes | Pais del cliente. |
| `firstName` | string | no | Primer nombre del cliente. |
| `lastName` | string | no | Apellido paterno del cliente. |
| `metadata` | string | no | Conjunto de pares llave-valor asociado al objeto. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bnpl_credit_currency": "string",
      "bnpl_credit_limit": 1,
      "country": "string",
      "created_at": "string",
      "disabled": true,
      "email": "ava@example.com",
      "email_validated": true,
      "first_name": "Ava",
      "id": "string",
      "last_name": "Chen",
      "object": "string",
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bnpl_credit_currency` | string | BNPL credit currency. |
| `bnpl_credit_limit` | number | BNPL credit limit. |
| `country` | string | Customer country code. |
| `created_at` | string | Customer creation timestamp. |
| `disabled` | boolean | Whether the customer is disabled. |
| `email` | string | Customer email address returned by Venti. |
| `email_validated` | boolean | Whether the customer email has been validated. |
| `first_name` | string | Customer first name. |
| `id` | string | Customer identifier. |
| `last_name` | string | Customer last name. |
| `object` | string | Response object type. |
| `updated_at` | string | Customer update timestamp. |

## Native endpoint

Through the native VentiPay API, this operation is `POST /customers` (base URL `https://api.ventipay.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-customer.md) for the provider-specific parameters and requirements.

