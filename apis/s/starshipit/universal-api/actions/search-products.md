# Starshipit: Search Products



```
GET https://connect.mindcloud.co/v1/universal/starshipit/latest/actions/search-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Starshipit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/starshipit/latest/actions/search-products?connectionId=$CONNECTION_ID&searchTerm=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "searchTerm": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/starshipit/latest/actions/search-products?${params}`, {
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
| `searchTerm` | string | yes | "" or "shoe" (Mandatory) |
| `pageNumber` | string | no |  |
| `pageSize` | string | no | Min: 10 Max: 2000 |
| `skipRecords` | string | no |  |
| `sortColumn` | string | no | Barcode \| BinLocation \| Brand \| Colour \| Country \| CustomsDescription \| DangerousGoodsType \| Height \| HSCode \| Length \| Manufacturer \| Materials \| Model \| Price \| Purpose \| Size \| Sku \| Title \| Weight \| Width |
| `sortDirection` | string | no | Ascending \| Descending |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "products": [
          {
            "binLocation": "string",
            "color": "string",
            "country": "string",
            "height": 1,
            "hsCode": "string",
            "id": 1,
            "length": 1,
            "price": 1,
            "size": "string",
            "sku": "string",
            "title": "string",
            "weight": 1,
            "width": 1
          }
        ],
        "success": true
      },
      "pageNumber": 1,
      "pageSize": 1,
      "succeeded": true,
      "totalPages": 1,
      "totalRecords": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `data.products` | array<object> |  |
| `data.products[].binLocation` | string |  |
| `data.products[].color` | string |  |
| `data.products[].country` | string |  |
| `data.products[].height` | number |  |
| `data.products[].hsCode` | string |  |
| `data.products[].id` | number |  |
| `data.products[].length` | number |  |
| `data.products[].price` | number |  |
| `data.products[].size` | string |  |
| `data.products[].sku` | string |  |
| `data.products[].title` | string |  |
| `data.products[].weight` | number |  |
| `data.products[].width` | number |  |
| `data.success` | boolean |  |
| `pageNumber` | number |  |
| `pageSize` | number |  |
| `succeeded` | boolean |  |
| `totalPages` | number |  |
| `totalRecords` | number |  |

## Native endpoint

Through the native Starshipit API, this operation is `GET /products` (base URL `https://api.starshipit.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-products.md) for the provider-specific parameters and requirements.

