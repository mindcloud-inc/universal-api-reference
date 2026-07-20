# Fiddle: List Inventory Locations

Retrieves inventory location records from Fiddle.

```
GET https://connect.mindcloud.co/v1/universal/fiddle/latest/actions/list-inventory-locations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fiddle `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fiddle/latest/actions/list-inventory-locations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fiddle/latest/actions/list-inventory-locations?${params}`, {
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
| `query` | string | no | Inventory location search query |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `inventoryLocationIds[]` | array<string> | no | Inventory location IDs |
| `siteIds[]` | array<string> | no | Site IDs |
| `sortBy` | string | no | Sort field |
| `sortDirection` | string | no | Sort direction |

## Response

```json
{
  "success": true,
  "data": [
    {
      "inventoryLocations": [
        {
          "createdAt": "2026-05-07T12:00:00.000Z",
          "id": "string",
          "name": "Ava Chen",
          "site": {
            "id": "string",
            "name": "Ava Chen"
          },
          "siteId": "string",
          "updatedAt": "2026-05-07T12:00:00.000Z"
        }
      ],
      "meta": {
        "page": 1,
        "size": 1,
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
| `inventoryLocations` | array<object> |  |
| `inventoryLocations[].createdAt` | date |  |
| `inventoryLocations[].id` | string |  |
| `inventoryLocations[].name` | string |  |
| `inventoryLocations[].site` | object |  |
| `inventoryLocations[].site.id` | string |  |
| `inventoryLocations[].site.name` | string |  |
| `inventoryLocations[].siteId` | string |  |
| `inventoryLocations[].updatedAt` | date |  |
| `meta` | object |  |
| `meta.page` | number |  |
| `meta.size` | number |  |
| `meta.total` | number |  |

## Native endpoint

Through the native Fiddle API, this operation is `GET /inventory-locations` (base URL `https://fiddle.io/rest/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-inventory-locations.md) for the provider-specific parameters and requirements.

