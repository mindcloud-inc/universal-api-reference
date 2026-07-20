# Fiddle: List Work Orders

Retrieves work order records from Fiddle.

```
GET https://connect.mindcloud.co/v1/universal/fiddle/latest/actions/list-work-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fiddle `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fiddle/latest/actions/list-work-orders?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fiddle/latest/actions/list-work-orders?${params}`, {
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
| `page` | number | no | Page number |
| `size` | number | no | Page size |
| `query` | string | no | Work order search query |
| `status` | string | no | Status selector |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `statuses` | string | no | Statuses selector |
| `customerId` | string | no | Customer ID selector |
| `inventoryItemId` | string | no | Inventory item ID selector |
| `archived` | boolean | no | Archived selector |
| `sortBy` | string | no | Sort field |
| `sortDirection` | string | no | Sort direction |

## Response

```json
{
  "success": true,
  "data": [
    {
      "meta": {
        "page": 1,
        "size": 1,
        "sortBy": "string",
        "sortDirection": "string",
        "total": 1
      },
      "workOrders": [
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
| `meta` | object |  |
| `meta.page` | number |  |
| `meta.size` | number |  |
| `meta.sortBy` | string |  |
| `meta.sortDirection` | string |  |
| `meta.total` | number |  |
| `workOrders` | array<object> |  |

## Native endpoint

Through the native Fiddle API, this operation is `GET /work-orders` (base URL `https://fiddle.io/rest/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-work-orders.md) for the provider-specific parameters and requirements.

