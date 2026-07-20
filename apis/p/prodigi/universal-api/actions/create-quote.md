# Prodigi: Create Quote

Retrieves Prodigi quotes for product and shipping costs.

```
GET https://connect.mindcloud.co/v1/universal/prodigi/latest/actions/create-quote
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Prodigi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/prodigi/latest/actions/create-quote?connectionId=$CONNECTION_ID&destinationCountryCode=GB&items%5B%5D=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "destinationCountryCode": "GB",
  "items[]": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/prodigi/latest/actions/create-quote?${params}`, {
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
| `destinationCountryCode` | string | yes | Two-letter ISO country code of the destination country. Example: `GB`. |
| `items[]` | array<object> | yes | Items to quote, including SKU, copies, attributes, and assets. Example: `[object Object]`. |
| `shippingMethod` | string | no | Requested shipping method: budget, standard, standardplus, express, or overnight. Example: `Budget`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `currencyCode` | string | no | Three-letter ISO currency code. Defaults to the merchant settings when omitted. Example: `GBP`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "costSummary": {},
      "items": [
        {}
      ],
      "shipmentMethod": "string",
      "shipments": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `costSummary` | object | Total item and shipping costs. |
| `items` | array<object> | Quoted items with generated quote item IDs. |
| `shipmentMethod` | string | Quoted shipping method. |
| `shipments` | array<object> | Expected shipment details and costs. |

## Native endpoint

Through the native Prodigi API, this operation is `POST /quotes` (base URL `https://api.prodigi.com/v4.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-quote.md) for the provider-specific parameters and requirements.

