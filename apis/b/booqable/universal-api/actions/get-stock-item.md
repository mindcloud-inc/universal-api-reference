# Booqable: Get Stock Item

Retrieves a stock item from Booqable.

```
GET https://connect.mindcloud.co/v1/universal/booqable/latest/actions/get-stock-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Booqable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/booqable/latest/actions/get-stock-item?connectionId=$CONNECTION_ID&id=218c1f4b-3124-4718-86e3-fc4646fe5562" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "218c1f4b-3124-4718-86e3-fc4646fe5562"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/booqable/latest/actions/get-stock-item?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Stock item ID. Example: `218c1f4b-3124-4718-86e3-fc4646fe5562`. |

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

Through the native Booqable API, this operation is `GET /stock_items/:id` (base URL `https://mindcloud.booqable.com/api/4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-stock-item.md) for the provider-specific parameters and requirements.

