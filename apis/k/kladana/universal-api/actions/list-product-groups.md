# Kladana: List Product Groups

Lists product groups in your Kladana account.

```
GET https://connect.mindcloud.co/v1/universal/kladana/latest/actions/list-product-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kladana `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kladana/latest/actions/list-product-groups?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kladana/latest/actions/list-product-groups?${params}`, {
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
      "archived": true,
      "code": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "externalCode": "string",
      "id": "string",
      "meta": {},
      "name": "Ava Chen",
      "pathName": "Ava Chen",
      "productFolder": {},
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
| `archived` | boolean | Whether the group is archived. |
| `code` | string | Internal code. |
| `created` | date | Creation timestamp. |
| `description` | string | Product group description. |
| `externalCode` | string | External code. |
| `id` | string | Product group UUID. |
| `meta` | object | Kladana metadata reference. |
| `name` | string | Product group name. |
| `pathName` | string | Folder path name. |
| `productFolder` | object | Parent product folder reference. |
| `shared` | boolean | Whether the group is shared. |
| `updated` | date | Last update timestamp. |

## Native endpoint

Through the native Kladana API, this operation is `GET /entity/productfolder` (base URL `https://api.kladana.com/api/remap/1.2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-product-groups.md) for the provider-specific parameters and requirements.

