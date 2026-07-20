# Understory: List Orders

Retrieves orders from Understory.

```
GET https://connect.mindcloud.co/v1/universal/understory/latest/actions/list-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Understory `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/understory/latest/actions/list-orders?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/understory/latest/actions/list-orders?${params}`, {
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
| `from` | date | no | Filter orders after this timestamp. |
| `to` | date | no | Filter orders before this timestamp. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
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
      "next": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items[].created_at` | date |  |
| `items[].customer.address.address_lines[]` | array<string> |  |
| `items[].customer.address.city` | string |  |
| `items[].customer.address.country` | string |  |
| `items[].customer.address.region` | string |  |
| `items[].customer.address.zip_code` | string |  |
| `items[].customer.company_name` | string |  |
| `items[].customer.customer_type` | string |  |
| `items[].customer.email` | string |  |
| `items[].customer.full_name` | string |  |
| `items[].customer.name` | string |  |
| `items[].customer.phone` | string |  |
| `items[].customer.vat_number` | string |  |
| `items[].id` | string |  |
| `items[].number` | string |  |
| `items[].origin.id` | string |  |
| `items[].origin.type` | string |  |
| `items[].status` | string |  |
| `items[].totals.amount.currency` | string |  |
| `items[].totals.amount.exponent` | number |  |
| `items[].totals.amount.value` | number |  |
| `items[].totals.discount.currency` | string |  |
| `items[].totals.discount.exponent` | number |  |
| `items[].totals.discount.value` | number |  |
| `items[].totals.vat_amount.currency` | string |  |
| `items[].totals.vat_amount.exponent` | number |  |
| `items[].totals.vat_amount.value` | number |  |
| `items[].updated_at` | date |  |
| `next` | string |  |

## Native endpoint

Through the native Understory API, this operation is `GET /v1/orders` (base URL `https://api.understory.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-orders.md) for the provider-specific parameters and requirements.

