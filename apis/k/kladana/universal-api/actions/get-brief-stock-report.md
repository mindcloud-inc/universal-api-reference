# Kladana: Get Brief Stock Report

Retrieves the brief stock report from Kladana.

```
GET https://connect.mindcloud.co/v1/universal/kladana/latest/actions/get-brief-stock-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kladana `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kladana/latest/actions/get-brief-stock-report?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kladana/latest/actions/get-brief-stock-report?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "article": "string",
      "assortment": {},
      "available": 1,
      "awaiting": 1,
      "code": "string",
      "inTransit": 1,
      "minPrice": 1,
      "name": "Ava Chen",
      "price": 1,
      "quantity": 1,
      "reserve": 1,
      "salePrice": 1,
      "stock": 1,
      "uom": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `article` | string | Article or SKU. |
| `assortment` | object | Assortment item reference. |
| `available` | number | Available quantity. |
| `awaiting` | number | Awaiting quantity. |
| `code` | string | Internal code. |
| `inTransit` | number | Quantity in transit. |
| `minPrice` | number | Minimum price value. |
| `name` | string | Assortment item name. |
| `price` | number | Price value. |
| `quantity` | number | Total quantity. |
| `reserve` | number | Reserved quantity. |
| `salePrice` | number | Sale price value. |
| `stock` | number | Current stock balance. |
| `uom` | object | Unit of measure. |

## Native endpoint

Through the native Kladana API, this operation is `GET /report/stock/all/current` (base URL `https://api.kladana.com/api/remap/1.2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-brief-stock-report.md) for the provider-specific parameters and requirements.

