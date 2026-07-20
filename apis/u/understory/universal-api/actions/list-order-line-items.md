# Understory: List Order Line Items

Retrieves order line items from Understory.

```
GET https://connect.mindcloud.co/v1/universal/understory/latest/actions/list-order-line-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Understory `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/understory/latest/actions/list-order-line-items?connectionId=$CONNECTION_ID&orderId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "orderId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/understory/latest/actions/list-order-line-items?${params}`, {
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
      "items": [
        {
          "details": {
            "experience_id": "string",
            "gift_card_id": "string",
            "ticket_id": "string",
            "type": "string"
          },
          "discounts": [
            {
              "amount": {
                "currency": "string",
                "exponent": 1,
                "value": 1
              },
              "code": "string",
              "type": "string"
            }
          ],
          "product_id": "string",
          "product_type": "string",
          "quantity": 1,
          "unit_price": {
            "currency": "string",
            "exponent": 1,
            "value": 1
          },
          "unit_vat_amount": {
            "currency": "string",
            "exponent": 1,
            "value": 1
          }
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items[].details.experience_id` | string |  |
| `items[].details.gift_card_id` | string |  |
| `items[].details.ticket_id` | string |  |
| `items[].details.type` | string |  |
| `items[].discounts[].amount.currency` | string |  |
| `items[].discounts[].amount.exponent` | number |  |
| `items[].discounts[].amount.value` | number |  |
| `items[].discounts[].code` | string |  |
| `items[].discounts[].type` | string |  |
| `items[].product_id` | string |  |
| `items[].product_type` | string |  |
| `items[].quantity` | number |  |
| `items[].unit_price.currency` | string |  |
| `items[].unit_price.exponent` | number |  |
| `items[].unit_price.value` | number |  |
| `items[].unit_vat_amount.currency` | string |  |
| `items[].unit_vat_amount.exponent` | number |  |
| `items[].unit_vat_amount.value` | number |  |

## Native endpoint

Through the native Understory API, this operation is `GET /v1/orders/{{orderId}}/line-items` (base URL `https://api.understory.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-order-line-items.md) for the provider-specific parameters and requirements.

