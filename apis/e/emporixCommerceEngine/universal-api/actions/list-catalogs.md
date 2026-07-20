# Emporix Commerce Engine: List Catalogs

Retrieves catalogs from Emporix Commerce Engine.

```
GET https://connect.mindcloud.co/v1/universal/emporixCommerceEngine/latest/actions/list-catalogs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Emporix Commerce Engine `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/emporixCommerceEngine/latest/actions/list-catalogs?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/emporixCommerceEngine/latest/actions/list-catalogs?${params}`, {
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
      "categoryIds": [
        "string"
      ],
      "description": "string",
      "id": "string",
      "metadata": {},
      "name": "Ava Chen",
      "publishedSites": [
        "string"
      ],
      "status": "string",
      "visibility": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `categoryIds` | array<string> |  |
| `description` | string |  |
| `id` | string |  |
| `metadata` | object |  |
| `name` | string |  |
| `publishedSites` | array<string> |  |
| `status` | string |  |
| `visibility` | object |  |

## Native endpoint

Through the native Emporix Commerce Engine API, this operation is `GET /catalog/{{credentials.tenantId}}/catalogs` (base URL `https://api.emporix.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-catalogs.md) for the provider-specific parameters and requirements.

