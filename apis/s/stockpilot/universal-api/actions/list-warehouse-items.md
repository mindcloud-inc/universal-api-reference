# Stockpilot: List Warehouse Items

Retrieves inventory items from a Stockpilot warehouse.

```
GET https://connect.mindcloud.co/v1/universal/stockpilot/latest/actions/list-warehouse-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stockpilot `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stockpilot/latest/actions/list-warehouse-items?connectionId=$CONNECTION_ID&limit=25&offset=0&uniqueId=9416324327" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "uniqueId": "9416324327"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stockpilot/latest/actions/list-warehouse-items?${params}`, {
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
| `uniqueId` | string | yes | Warehouse unique ID Example: `9416324327`. |
| `page` | number | no | Page number Default: `1`. |
| `pageSize` | number | no | Number of items per page Default: `100`. |
| `sku` | string | no | Filter by SKU Example: `COD-INV-20260401-1738`. |
| `barcode` | string | no | Filter by barcode Example: `5901234123458`. |

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
| `count` | number |  |
| `current_page` | number |  |
| `next` | boolean |  |
| `previous` | boolean |  |
| `results` | array<object> |  |
| `total_pages` | number |  |

## Native endpoint

Through the native Stockpilot API, this operation is `GET /warehouses/:unique_id/items` (base URL `https://api.stockpilot.dev`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-warehouse-items.md) for the provider-specific parameters and requirements.

