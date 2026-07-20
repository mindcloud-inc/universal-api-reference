# InventoryBase: List Clients

Retrieves all client records from InventoryBase.

```
GET https://connect.mindcloud.co/v1/universal/inventoryBase/latest/actions/list-clients
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InventoryBase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/inventoryBase/latest/actions/list-clients?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/inventoryBase/latest/actions/list-clients?${params}`, {
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
            "line1": "string",
            "postcode": "string"
          },
          "company": "string",
          "createdAt": "string",
          "customFields": {},
          "email": "ava@example.com",
          "emailNotifications": true,
          "id": 1,
          "name": "Ava Chen",
          "telephone": "string"
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
| `data[].address.line1` | string |  |
| `data[].address.postcode` | string |  |
| `data[].company` | string |  |
| `data[].createdAt` | string |  |
| `data[].customFields` | object |  |
| `data[].email` | string |  |
| `data[].emailNotifications` | boolean |  |
| `data[].id` | number |  |
| `data[].name` | string |  |
| `data[].telephone` | string |  |
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

Through the native InventoryBase API, this operation is `GET /clients` (base URL `https://api.inventorybase.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-clients.md) for the provider-specific parameters and requirements.

