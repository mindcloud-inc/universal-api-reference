# MoySklad: List products

Retrieves products from MoySklad.

```
GET https://connect.mindcloud.co/v1/universal/moySklad/latest/actions/list-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MoySklad `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moySklad/latest/actions/list-products?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moySklad/latest/actions/list-products?${params}`, {
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
      "code": "string",
      "context": {},
      "externalCode": "string",
      "id": "string",
      "meta": {},
      "name": "Ava Chen",
      "rows": [
        {}
      ],
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string | Product code. |
| `context` | object | MoySklad response context metadata. |
| `externalCode` | string | External code. |
| `id` | string | Product identifier when rows are flattened by mapper. |
| `meta` | object | Collection metadata including href, type, mediaType, size, limit, and offset. |
| `name` | string | Product name. |
| `rows` | array<object> | Product records returned by MoySklad. |
| `updated` | date | Last updated timestamp. |

## Native endpoint

Through the native MoySklad API, this operation is `GET entity/product` (base URL `https://api.moysklad.ru/api/remap/1.2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-products.md) for the provider-specific parameters and requirements.

