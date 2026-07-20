# NetSuite - Basic: List Inventory Items

Retrieves a list of inventory items from NetSuite.

```
GET https://connect.mindcloud.co/v1/universal/netSuiteBasic/latest/actions/list-inventory-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetSuite - Basic `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/netSuiteBasic/latest/actions/list-inventory-items?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/netSuiteBasic/latest/actions/list-inventory-items?${params}`, {
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
      "__meta": {
        "presentation": {
          "entityUrl": "https://example.com",
          "fields": {
            "id": "string",
            "name": "Ava Chen"
          },
          "type": "string"
        }
      },
      "id": "string",
      "links": [
        {
          "href": "https://example.com",
          "method": "https://example.com",
          "rel": "https://example.com"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `__meta` | object |  |
| `__meta.presentation` | object |  |
| `__meta.presentation.entityUrl` | string |  |
| `__meta.presentation.fields` | object |  |
| `__meta.presentation.fields.id` | string |  |
| `__meta.presentation.fields.name` | string |  |
| `__meta.presentation.type` | string |  |
| `id` | string |  |
| `links` | array<object> |  |
| `links[].href` | string |  |
| `links[].method` | string |  |
| `links[].rel` | string |  |

## Native endpoint

Through the native NetSuite - Basic API, this operation is `GET /record/v1/inventoryItem` (base URL `https://{{credentials.accountDomain}}.suitetalk.api.netsuite.com/services/rest`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-inventory-items.md) for the provider-specific parameters and requirements.

