# Cloudprinter.com: Get Order Quote

Retrieves an order quote from Cloudprinter.com.

```
GET https://connect.mindcloud.co/v1/universal/cloudprintercom/latest/actions/get-order-quote
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudprinter.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudprintercom/latest/actions/get-order-quote?connectionId=$CONNECTION_ID&country=string&items%5B%5D=%5Bobject%20Object%5D&items%5B%5D.reference=string&items%5B%5D.product=string&items%5B%5D.count=string&items%5B%5D.options%5B%5D.type=string&items%5B%5D.options%5B%5D.count=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "country": "string",
  "items[]": "[object Object]",
  "items[].reference": "string",
  "items[].product": "string",
  "items[].count": "string",
  "items[].options[].type": "string",
  "items[].options[].count": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudprintercom/latest/actions/get-order-quote?${params}`, {
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
| `country` | string | yes | Destination country in ISO 3166-1 alpha-2 format. |
| `state` | string | no | Destination state or region code when required for the selected country. |
| `currency` | string | no | Optional quote currency in ISO 4217 format. |
| `items[]` | array<object> | yes | One or more items to quote. |
| `items[].reference` | string | yes | Client-side reference for this quote item. |
| `items[].product` | string | yes | Cloudprinter product reference. |
| `items[].count` | string | yes | Quantity for this quote item. |
| `items[].options[]` | array<object> | no | Optional item options. Cloudprinter currently expects an array value even when empty. Default: `[]`. |
| `items[].options[].type` | string | yes | Option type from product info. |
| `items[].options[].count` | string | yes | Quantity for the selected option. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "currency": "string",
      "expire_date": "string",
      "invoice_currency": "string",
      "invoice_exchange_rate": "string",
      "price": "string",
      "production_sla_days": 1,
      "shipments": [
        [
          {}
        ]
      ],
      "subtotals": {
        "app_fee": "string",
        "currency": "string",
        "fee": "string",
        "items": "string"
      },
      "vat": "string",
      "vat_rate": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currency` | string |  |
| `expire_date` | string |  |
| `invoice_currency` | string |  |
| `invoice_exchange_rate` | string |  |
| `price` | string |  |
| `production_sla_days` | number |  |
| `shipments[]` | array<object> |  |
| `shipments[].items[]` | array<object> |  |
| `shipments[].items[].reference` | string |  |
| `shipments[].quotes[]` | array<object> |  |
| `shipments[].quotes[].currency` | string |  |
| `shipments[].quotes[].price` | string |  |
| `shipments[].quotes[].quote` | string |  |
| `shipments[].quotes[].service` | string |  |
| `shipments[].quotes[].shipping_level` | string |  |
| `shipments[].quotes[].shipping_option` | string |  |
| `shipments[].quotes[].vat` | string |  |
| `shipments[].total_weight` | string |  |
| `subtotals` | object |  |
| `subtotals.app_fee` | string |  |
| `subtotals.currency` | string |  |
| `subtotals.fee` | string |  |
| `subtotals.items` | string |  |
| `vat` | string |  |
| `vat_rate` | number |  |

## Native endpoint

Through the native Cloudprinter.com API, this operation is `POST /cloudcore/1.0/orders/quote` (base URL `https://api.cloudprinter.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-order-quote.md) for the provider-specific parameters and requirements.

