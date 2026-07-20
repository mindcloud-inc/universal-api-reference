# Fiddle: List Inventory Items

Retrieves inventory item records from Fiddle.

```
GET https://connect.mindcloud.co/v1/universal/fiddle/latest/actions/list-inventory-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fiddle `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fiddle/latest/actions/list-inventory-items?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fiddle/latest/actions/list-inventory-items?${params}`, {
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
| `query` | string | no | Inventory item search query |
| `status` | string | no | Status selector |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `inventoryTypeId` | string | no | Inventory type ID selector |
| `supplierId` | string | no | Supplier ID selector |
| `inventoryTypeIds[]` | array<string> | no | Inventory type ID list |
| `exclude[]` | array<string> | no | Inventory item IDs to exclude |
| `exactMatch` | boolean | no | Whether to exact-match the query |
| `hideEmpty` | boolean | no | Hide empty inventory items |
| `inventoryLocations[]` | array<string> | no | Inventory location IDs |
| `hasMasterFormula` | boolean | no | Whether the item has a master formula |
| `hasMasterBillOfMaterial` | boolean | no | Whether the item has a master bill of material |
| `startDate` | date | no | Start date |
| `endDate` | date | no | End date |
| `showOnlyNonZeroTotalValue` | boolean | no | Show only items with non-zero total value |
| `archived` | boolean | no | Archived selector |
| `excludeStatuses[]` | array<string> | no | Statuses to exclude |
| `sortBy` | string | no | Sort field |
| `sortDirection` | string | no | Sort direction |

## Response

```json
{
  "success": true,
  "data": [
    {
      "inventoryItems": [
        {}
      ],
      "meta": {
        "count": 1,
        "from": 1,
        "lastPage": 1,
        "page": 1,
        "query": "string",
        "size": 1,
        "sortBy": "string",
        "sortDirection": "string",
        "to": 1,
        "total": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `inventoryItems` | array<object> |  |
| `meta` | object |  |
| `meta.count` | number |  |
| `meta.from` | number |  |
| `meta.lastPage` | number |  |
| `meta.page` | number |  |
| `meta.query` | string |  |
| `meta.size` | number |  |
| `meta.sortBy` | string |  |
| `meta.sortDirection` | string |  |
| `meta.to` | number |  |
| `meta.total` | number |  |

## Native endpoint

Through the native Fiddle API, this operation is `GET /inventory-items` (base URL `https://fiddle.io/rest/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-inventory-items.md) for the provider-specific parameters and requirements.

