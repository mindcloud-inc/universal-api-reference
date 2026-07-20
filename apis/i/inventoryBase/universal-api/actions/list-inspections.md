# InventoryBase: List Inspections

Retrieves all inspection records from InventoryBase.

```
GET https://connect.mindcloud.co/v1/universal/inventoryBase/latest/actions/list-inspections
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InventoryBase `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/inventoryBase/latest/actions/list-inspections?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/inventoryBase/latest/actions/list-inspections?${params}`, {
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
      "data": [
        {
          "createdAt": "string",
          "id": 1,
          "property": {
            "id": 1,
            "ref": "string"
          },
          "reportKey": "string",
          "state": {
            "id": 1,
            "name": "Ava Chen"
          },
          "type": {
            "id": 1,
            "name": "Ava Chen"
          },
          "updatedAt": "string",
          "uuid": "string"
        }
      ],
      "links": {
        "first": "https://example.com",
        "last": "https://example.com",
        "next": "https://example.com",
        "prev": "https://example.com",
        "self": "https://example.com"
      },
      "pagination": {
        "currentPage": 1,
        "perPage": 1,
        "totalPages": 1,
        "totalRecords": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `data[].createdAt` | string |  |
| `data[].id` | number |  |
| `data[].property` | object |  |
| `data[].property.id` | number |  |
| `data[].property.ref` | string |  |
| `data[].reportKey` | string |  |
| `data[].state` | object |  |
| `data[].state.id` | number |  |
| `data[].state.name` | string |  |
| `data[].type` | object |  |
| `data[].type.id` | number |  |
| `data[].type.name` | string |  |
| `data[].updatedAt` | string |  |
| `data[].uuid` | string |  |
| `links` | object |  |
| `links.first` | string |  |
| `links.last` | string |  |
| `links.next` | string |  |
| `links.prev` | string |  |
| `links.self` | string |  |
| `pagination` | object |  |
| `pagination.currentPage` | number |  |
| `pagination.perPage` | number |  |
| `pagination.totalPages` | number |  |
| `pagination.totalRecords` | number |  |

## Native endpoint

Through the native InventoryBase API, this operation is `GET /inspections` (base URL `https://api.inventorybase.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-inspections.md) for the provider-specific parameters and requirements.

