# Printify: List Products

Retrieves products from a Printify shop.

```
GET https://connect.mindcloud.co/v1/universal/printify/latest/actions/list-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Printify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/printify/latest/actions/list-products?connectionId=$CONNECTION_ID&shopId=27141936" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "shopId": "27141936"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/printify/latest/actions/list-products?${params}`, {
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
| `limit` | number | no | Maximum number of products to return. |
| `page` | number | no | Result page to fetch. |
| `shopId` | number | yes | Printify shop id. Default: `27141936`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "currentPage": 1,
      "data": [
        {
          "blueprintId": 1,
          "id": "string",
          "printProviderId": 1,
          "title": "string",
          "visible": true
        }
      ],
      "perPage": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currentPage` | number |  |
| `data` | array<object> |  |
| `data[].blueprintId` | number |  |
| `data[].id` | string |  |
| `data[].printProviderId` | number |  |
| `data[].title` | string |  |
| `data[].visible` | boolean |  |
| `perPage` | number |  |
| `total` | number |  |

## Native endpoint

Through the native Printify API, this operation is `GET /shops/:shop_id/products.json` (base URL `https://api.printify.com/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-products.md) for the provider-specific parameters and requirements.

