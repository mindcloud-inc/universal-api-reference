# Kladana: List Assortment

Lists assortment items in your Kladana account.

```
GET https://connect.mindcloud.co/v1/universal/kladana/latest/actions/list-assortment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kladana `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kladana/latest/actions/list-assortment?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kladana/latest/actions/list-assortment?${params}`, {
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
      "article": "string",
      "buyPrice": {},
      "code": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "externalCode": "string",
      "id": "string",
      "meta": {},
      "name": "Ava Chen",
      "pathName": "Ava Chen",
      "salePrices": [
        {}
      ],
      "shared": true,
      "type": "string",
      "uom": {},
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean | Whether the item is archived. |
| `article` | string | SKU or article value. |
| `buyPrice` | object | Buy price. |
| `code` | string | Internal code. |
| `created` | date | Creation timestamp. |
| `externalCode` | string | External code. |
| `id` | string | Assortment item UUID. |
| `meta` | object | Kladana metadata reference. |
| `name` | string | Assortment item name. |
| `pathName` | string | Folder path name. |
| `salePrices` | array<object> | Sale prices. |
| `shared` | boolean | Whether the item is shared. |
| `type` | string | Assortment item type. |
| `uom` | object | Unit of measure. |
| `updated` | date | Last update timestamp. |

## Native endpoint

Through the native Kladana API, this operation is `GET /entity/assortment` (base URL `https://api.kladana.com/api/remap/1.2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-assortment.md) for the provider-specific parameters and requirements.

