# Kiwify: Get Sale

Retrieves a sale from Kiwify.

```
GET https://connect.mindcloud.co/v1/universal/kiwify/latest/actions/get-sale
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kiwify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kiwify/latest/actions/get-sale?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kiwify/latest/actions/get-sale?${params}`, {
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
| `id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "affiliate_commission": {},
      "approved_date": "string",
      "boleto_url": "https://example.com",
      "card_last_digits": "string",
      "card_rejection_reason": "string",
      "card_type": "string",
      "created_at": "string",
      "customer": {},
      "id": "string",
      "installments": 1,
      "is_one_click": true,
      "net_amount": 1,
      "parent_order_id": "string",
      "payment": {},
      "payment_method": "string",
      "product": {},
      "reference": "string",
      "refunded_at": "string",
      "revenue_partners": [
        "string"
      ],
      "sale_type": "string",
      "status": "string",
      "tracking": {},
      "two_cards": true,
      "type": "string",
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `affiliate_commission` | object |  |
| `approved_date` | string |  |
| `boleto_url` | string |  |
| `card_last_digits` | string |  |
| `card_rejection_reason` | string |  |
| `card_type` | string |  |
| `created_at` | string |  |
| `customer` | object |  |
| `id` | string |  |
| `installments` | number |  |
| `is_one_click` | boolean |  |
| `net_amount` | number |  |
| `parent_order_id` | string |  |
| `payment` | object |  |
| `payment_method` | string |  |
| `product` | object |  |
| `reference` | string |  |
| `refunded_at` | string |  |
| `revenue_partners` | array<string> |  |
| `sale_type` | string |  |
| `status` | string |  |
| `tracking` | object |  |
| `two_cards` | boolean |  |
| `type` | string |  |
| `updated_at` | string |  |

## Native endpoint

Through the native Kiwify API, this operation is `GET /v1/sales/:id` (base URL `https://public-api.kiwify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sale.md) for the provider-specific parameters and requirements.

