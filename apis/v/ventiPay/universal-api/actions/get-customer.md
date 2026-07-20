# VentiPay: Get Customer

Retrieves a customer from VentiPay.

```
GET https://connect.mindcloud.co/v1/universal/ventiPay/latest/actions/get-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a VentiPay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ventiPay/latest/actions/get-customer?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ventiPay/latest/actions/get-customer?${params}`, {
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
| `id` | string | yes | Venti customer identifier. |

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
      "language": "string",
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
| `email` | string | Customer email address. |
| `email_validated` | boolean | Whether the customer email has been validated. |
| `first_name` | string | Customer first name. |
| `id` | string | Customer identifier. |
| `language` | string | Customer language. |
| `last_name` | string | Customer last name. |
| `object` | string | Response object type. |
| `updated_at` | string | Customer update timestamp. |

## Native endpoint

Through the native VentiPay API, this operation is `GET /customers/:id` (base URL `https://api.ventipay.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-customer.md) for the provider-specific parameters and requirements.

