# Booqable: Update Stock Item

Updates an existing stock item in Booqable.

```
PUT https://connect.mindcloud.co/v1/universal/booqable/latest/actions/update-stock-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Booqable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/booqable/latest/actions/update-stock-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "96e16eb3-614f-4a6a-8444-531244376f3a",
  "data": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/booqable/latest/actions/update-stock-item', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "96e16eb3-614f-4a6a-8444-531244376f3a",
    "data": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Stock item ID. Example: `96e16eb3-614f-4a6a-8444-531244376f3a`. |
| `data` | object | yes | Stock item payload. Enter the inner JSON:API resource object; the path ID must match the stock item being updated. Example: `[object Object]`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `include` | string | no | Comma-separated relationships to sideload, for example barcode,location,properties. Example: `barcode,location,properties`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "archived": true,
        "createdAt": "2026-05-07T12:00:00.000Z",
        "identifier": "string",
        "status": "string",
        "stockItemType": "string",
        "updatedAt": "2026-05-07T12:00:00.000Z"
      },
      "id": "string",
      "relationships": {},
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.archived` | boolean | Whether the stock item is archived. |
| `attributes.createdAt` | date | When the stock item was created. |
| `attributes.identifier` | string | Stock item identifier. |
| `attributes.status` | string | Current stock item status. |
| `attributes.stockItemType` | string | Stock item type. |
| `attributes.updatedAt` | date | When the stock item was last updated. |
| `id` | string | Stock item ID. |
| `relationships` | object | Stock item relationships. |
| `type` | string | Resource type. |

## Native endpoint

Through the native Booqable API, this operation is `PUT /stock_items/:id` (base URL `https://mindcloud.booqable.com/api/4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-stock-item.md) for the provider-specific parameters and requirements.

