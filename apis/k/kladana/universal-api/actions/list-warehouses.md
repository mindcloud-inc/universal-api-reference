# Kladana: List Warehouses

Lists warehouses in your Kladana account.

```
GET https://connect.mindcloud.co/v1/universal/kladana/latest/actions/list-warehouses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kladana `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kladana/latest/actions/list-warehouses?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kladana/latest/actions/list-warehouses?${params}`, {
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
      "address": "string",
      "archived": true,
      "code": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "externalCode": "string",
      "id": "string",
      "meta": {},
      "name": "Ava Chen",
      "parent": {},
      "shared": true,
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string | Warehouse address. |
| `archived` | boolean | Whether the warehouse is archived. |
| `code` | string | Internal code. |
| `created` | date | Creation timestamp. |
| `description` | string | Warehouse description. |
| `externalCode` | string | External code. |
| `id` | string | Warehouse UUID. |
| `meta` | object | Kladana metadata reference. |
| `name` | string | Warehouse name. |
| `parent` | object | Parent warehouse reference. |
| `shared` | boolean | Whether the warehouse is shared. |
| `updated` | date | Last update timestamp. |

## Native endpoint

Through the native Kladana API, this operation is `GET /entity/store` (base URL `https://api.kladana.com/api/remap/1.2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-warehouses.md) for the provider-specific parameters and requirements.

