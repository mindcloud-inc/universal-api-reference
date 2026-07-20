# Mercado Pago: Create Preference

Creates a checkout preference in Mercado Pago.

```
POST https://connect.mindcloud.co/v1/universal/mercadoPago/latest/actions/create-preference
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mercado Pago `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mercadoPago/latest/actions/create-preference" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "items[]": [
    {}
  ],
  "items[].title": "string",
  "items[].quantity": 1,
  "items[].unit_price": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mercadoPago/latest/actions/create-preference', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "items[]": [{}],
    "items[].title": "string",
    "items[].quantity": 1,
    "items[].unit_price": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `items[]` | array<object> | yes |  |
| `items[].title` | string | yes |  |
| `items[].quantity` | number | yes |  |
| `items[].unit_price` | number | yes |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `items[].currency_id` | string | no |  |
| `payer` | object | no |  |
| `payer.email` | string | no |  |
| `payer.first_name` | string | no |  |
| `payer.last_name` | string | no |  |
| `payment_methods` | object | no |  |
| `payment_methods.installments` | number | no |  |
| `payment_methods.default_payment_method_id` | string | no |  |
| `payment_methods.default_installments` | number | no |  |
| `payment_methods.default_payment_type_id` | string | no |  |
| `payment_methods.excluded_payment_methods[]` | array<object> | no |  |
| `payment_methods.excluded_payment_methods[].id` | string | no |  |
| `payment_methods.excluded_payment_types[]` | array<object> | no |  |
| `payment_methods.excluded_payment_types[].id` | string | no |  |
| `back_urls` | object | no |  |
| `back_urls.success` | string | no |  |
| `back_urls.pending` | string | no |  |
| `back_urls.failure` | string | no |  |
| `notification_url` | string | no | Use an HTTPS callback URL. |
| `external_reference` | string | no |  |
| `auto_return` | string | no | Default: `approved`. |
| `binary_mode` | boolean | no |  |
| `expires` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "init_point": "string",
      "sandbox_init_point": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `init_point` | string |  |
| `sandbox_init_point` | string |  |

## Native endpoint

Through the native Mercado Pago API, this operation is `POST /checkout/preferences` (base URL `https://api.mercadopago.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-preference.md) for the provider-specific parameters and requirements.

