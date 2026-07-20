# Stockpilot: List Products

Retrieves products from Stockpilot.

```
GET https://connect.mindcloud.co/v1/universal/stockpilot/latest/actions/list-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stockpilot `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stockpilot/latest/actions/list-products?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stockpilot/latest/actions/list-products?${params}`, {
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
| `page` | number | no | Page number Default: `1`. |
| `pageSize` | number | no | Items per page Default: `100`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "current_page": 1,
      "next": true,
      "previous": true,
      "results": [
        {}
      ],
      "total_pages": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number | Number of products returned |
| `current_page` | number | Current page number |
| `next` | boolean | Whether another page exists |
| `previous` | boolean | Whether a previous page exists |
| `results` | array<object> | Product result rows |
| `total_pages` | number | Total number of pages |

## Native endpoint

Through the native Stockpilot API, this operation is `GET /products` (base URL `https://api.stockpilot.dev`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-products.md) for the provider-specific parameters and requirements.

