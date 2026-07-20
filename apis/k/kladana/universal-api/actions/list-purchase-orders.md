# Kladana: List Purchase Orders

Lists purchase orders in your Kladana account.

```
GET https://connect.mindcloud.co/v1/universal/kladana/latest/actions/list-purchase-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kladana `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kladana/latest/actions/list-purchase-orders?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kladana/latest/actions/list-purchase-orders?${params}`, {
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
      "agent": {},
      "applicable": true,
      "attributes": [
        {}
      ],
      "created": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "externalCode": "string",
      "group": {},
      "id": "string",
      "meta": {},
      "moment": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "organization": {},
      "owner": {},
      "positions": {},
      "printed": true,
      "published": true,
      "state": {},
      "store": {},
      "sum": 1,
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agent` | object | Counterparty reference. |
| `applicable` | boolean | Whether the document is applicable. |
| `attributes` | array<object> | Custom attributes. |
| `created` | date | Creation timestamp. |
| `description` | string | Document description. |
| `externalCode` | string | External code. |
| `group` | object | Group reference. |
| `id` | string | Document UUID. |
| `meta` | object | Kladana metadata reference. |
| `moment` | date | Document moment. |
| `name` | string | Document name or number. |
| `organization` | object | Organization reference. |
| `owner` | object | Owner reference. |
| `positions` | object | Positions collection reference. |
| `printed` | boolean | Whether the document was printed. |
| `published` | boolean | Whether the document was published. |
| `state` | object | Workflow state reference. |
| `store` | object | Warehouse reference. |
| `sum` | number | Document total amount. |
| `updated` | date | Last update timestamp. |

## Native endpoint

Through the native Kladana API, this operation is `GET /entity/purchaseorder` (base URL `https://api.kladana.com/api/remap/1.2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-purchase-orders.md) for the provider-specific parameters and requirements.

