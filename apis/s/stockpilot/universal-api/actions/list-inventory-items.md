# Stockpilot: List Inventory Items

Retrieves inventory items from Stockpilot.

```
GET https://connect.mindcloud.co/v1/universal/stockpilot/latest/actions/list-inventory-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stockpilot `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stockpilot/latest/actions/list-inventory-items?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stockpilot/latest/actions/list-inventory-items?${params}`, {
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
| `pageSize` | number | no | Number of items per page Default: `100`. |
| `createdAt` | string | no | Filter by creation date in YYYY-MM-DD format Example: `2026-04-01`. |

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

Through the native Stockpilot API, this operation is `GET /inventory` (base URL `https://api.stockpilot.dev`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-inventory-items.md) for the provider-specific parameters and requirements.

