# Understory: Get Order

Retrieves an order from Understory.

```
GET https://connect.mindcloud.co/v1/universal/understory/latest/actions/get-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Understory `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/understory/latest/actions/get-order?connectionId=$CONNECTION_ID&orderId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "orderId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/understory/latest/actions/get-order?${params}`, {
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
| `orderId` | string | yes | The unique identifier of the order. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "customer": {
        "address": {
          "address_lines": [
            [
              "string"
            ]
          ],
          "city": "string",
          "country": "string",
          "region": "string",
          "zip_code": "string"
        },
        "company_name": "Ava Chen",
        "customer_type": "string",
        "email": "ava@example.com",
        "full_name": "Ava Chen",
        "name": "Ava Chen",
        "phone": "string",
        "vat_number": "string"
      },
      "id": "string",
      "number": "string",
      "origin": {
        "id": "string",
        "type": "string"
      },
      "status": "string",
      "totals": {
        "amount": {
          "currency": "string",
          "exponent": 1,
          "value": 1
        },
        "discount": {
          "currency": "string",
          "exponent": 1,
          "value": 1
        },
        "vat_amount": {
          "currency": "string",
          "exponent": 1,
          "value": 1
        }
      },
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date |  |
| `customer.address.address_lines[]` | array<string> |  |
| `customer.address.city` | string |  |
| `customer.address.country` | string |  |
| `customer.address.region` | string |  |
| `customer.address.zip_code` | string |  |
| `customer.company_name` | string |  |
| `customer.customer_type` | string |  |
| `customer.email` | string |  |
| `customer.full_name` | string |  |
| `customer.name` | string |  |
| `customer.phone` | string |  |
| `customer.vat_number` | string |  |
| `id` | string |  |
| `number` | string |  |
| `origin.id` | string |  |
| `origin.type` | string |  |
| `status` | string |  |
| `totals.amount.currency` | string |  |
| `totals.amount.exponent` | number |  |
| `totals.amount.value` | number |  |
| `totals.discount.currency` | string |  |
| `totals.discount.exponent` | number |  |
| `totals.discount.value` | number |  |
| `totals.vat_amount.currency` | string |  |
| `totals.vat_amount.exponent` | number |  |
| `totals.vat_amount.value` | number |  |
| `updated_at` | date |  |

## Native endpoint

Through the native Understory API, this operation is `GET /v1/orders/{{orderId}}` (base URL `https://api.understory.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-order.md) for the provider-specific parameters and requirements.

