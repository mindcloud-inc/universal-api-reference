# Goodbarber eCommerce: Get Order



```
GET https://connect.mindcloud.co/v1/universal/goodbarberECommerce/latest/actions/get-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Goodbarber eCommerce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goodbarberECommerce/latest/actions/get-order?connectionId=$CONNECTION_ID&orderId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "orderId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goodbarberECommerce/latest/actions/get-order?${params}`, {
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
| `orderId` | number | yes | Unique ID of the order. Default: `1`. Example: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "currency": "string",
      "customer_note": "string",
      "discount": "string",
      "email": "ava@example.com",
      "first_name": "Ava",
      "has_invoice": true,
      "id": 1,
      "invoice_num": 1,
      "items": [
        {}
      ],
      "last_name": "Chen",
      "order_num": 1,
      "payment_mode": "string",
      "payment_type": "string",
      "phone": "string",
      "pricing_details": {},
      "promo_code": 1,
      "receipt_num": 1,
      "selected_delivery_slot": {},
      "shipping_address": {},
      "shipping_amount": "string",
      "shipping_method": "string",
      "shipping_tax_amount": "string",
      "shipping_tax_rate": "string",
      "shipping_type": "string",
      "status": "string",
      "subtotal": "string",
      "tax_amount": "string",
      "tax_mode": "string",
      "tax_rate": "string",
      "total": "string",
      "updated_at": "string",
      "user_id": 1,
      "vat_number": "string",
      "weight": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string | <div class="field_description">Timestamp of the order creation.</div> |
| `currency` | string | <div class="field_description">Currency related to the amount of the order</div> |
| `customer_note` | string | <div class="field_description">Note providing additional informations, written by the customer during his order process.</div> |
| `discount` | string | <div class="field_description">Amount discounted off the order total thanks to promo code</div> |
| `email` | string | <div class="field_description">Email provided by client</div> |
| `first_name` | string | <div class="field_description">First name of the client</div> |
| `has_invoice` | boolean | <div class="field_description">Flag which indicates if the order has an associated invoice</div> |
| `id` | number | <div class="field_description">Unique ID of the order.</div> |
| `invoice_num` | number | <div class="field_description">Number related to the invoice of the order</div> |
| `items` | array<object> | <div class="field_description">List of items ordered by the end customer. Each of these items is a variant of a specific product, in other words a version of that product with specific characteristics (color, size, etc).</div> |
| `last_name` | string | <div class="field_description">Last name of the client</div> |
| `order_num` | number | <div class="field_description">Auto-incremented order ID (used for frontend display).</div> |
| `payment_mode` | string | <div class="field_description">Mode used to pay the order.<br>It'll be <strong>'live'</strong> if the payment is processed in production<br>It'll be <strong>'test'</strong> if the payment is processed in test mode</div> |
| `payment_type` | string | <div class="field_description">Method used to pay the order.<br>It can be <strong>'paypal', 'one_click_payment', 'stripe_no_cb', 'stripe_cb_three_d_secure', 'stripe_cb', 'mercado'</strong> for online production mode<br>It can be <strong>'sandbox'</strong> for test mode<br>It can be <strong>'offline'</strong> for offline production mode</div> |
| `phone` | string | <div class="field_description">Phone provided by client</div> |
| `pricing_details` | object |  |
| `promo_code` | number | <div class="field_description">Unique ID of the promo code used, if applicable</div> |
| `receipt_num` | number | <div class="field_description">Number related to the receipt of the order</div> |
| `selected_delivery_slot` | object |  |
| `shipping_address` | object |  |
| `shipping_amount` | string | <div class="field_description">Amount related to the cost of the shipping of the order</div> |
| `shipping_method` | string | <div class="field_description">Shipping method name used for order delivery</div> |
| `shipping_tax_amount` | string | <div class="field_description">Tax amount related to the cost of the shipping of the order</div> |
| `shipping_tax_rate` | string | <div class="field_description">Tax rate applied to the cost of the shipping of the order</div> |
| `shipping_type` | string |  |
| `status` | string |  |
| `subtotal` | string | <div class="field_description">Amount of the order used for taxes computations.</div> |
| `tax_amount` | string | <div class="field_description">Tax amount related to the amount of the order</div> |
| `tax_mode` | string |  |
| `tax_rate` | string | <div class="field_description">Tax rate applied to compute tax amount of the order</div> |
| `total` | string | <div class="field_description">Total amount of the order (taxes and shipping included).</div> |
| `updated_at` | string | <div class="field_description">Timestamp of the order last update.</div> |
| `user_id` | number | <div class="field_description">Contains the ID of the user if the order was made by a logged user, None otherwise.</div> |
| `vat_number` | string | <div class="field_description">VAT number of the order</div> |
| `weight` | number | <div class="field_description">Total weight of the ordered items (unit: kg).</div></div> |

## Native endpoint

Through the native Goodbarber eCommerce API, this operation is `GET /publicapi/v2/general/orders/:webzine_id/order/:order_id/` (base URL `https://commerce.goodbarber.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-order.md) for the provider-specific parameters and requirements.

