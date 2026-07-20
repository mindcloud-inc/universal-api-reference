# InventoryBase: List Properties

Retrieves all property records from InventoryBase.

```
GET https://connect.mindcloud.co/v1/universal/inventoryBase/latest/actions/list-properties
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InventoryBase `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/inventoryBase/latest/actions/list-properties?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/inventoryBase/latest/actions/list-properties?${params}`, {
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
          "address": {
            "city": "string",
            "country": "string",
            "line1": "string",
            "postcode": "string"
          },
          "customFields": {},
          "furnished": "string",
          "garden": true,
          "id": 1,
          "noOfBaths": 1,
          "noOfBeds": 1,
          "noOfGarages": 1,
          "parentPropertyId": 1,
          "parking": true,
          "propertyType": {
            "id": 1,
            "title": "string"
          },
          "ref": "string",
          "type": "string"
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
| `data[].address` | object |  |
| `data[].address.city` | string |  |
| `data[].address.country` | string |  |
| `data[].address.line1` | string |  |
| `data[].address.postcode` | string |  |
| `data[].customFields` | object |  |
| `data[].furnished` | string |  |
| `data[].garden` | boolean |  |
| `data[].id` | number |  |
| `data[].noOfBaths` | number |  |
| `data[].noOfBeds` | number |  |
| `data[].noOfGarages` | number |  |
| `data[].parentPropertyId` | number |  |
| `data[].parking` | boolean |  |
| `data[].propertyType` | object |  |
| `data[].propertyType.id` | number |  |
| `data[].propertyType.title` | string |  |
| `data[].ref` | string |  |
| `data[].type` | string |  |
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

Through the native InventoryBase API, this operation is `GET /properties` (base URL `https://api.inventorybase.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-properties.md) for the provider-specific parameters and requirements.

