# EenvoudigFactureren: List Invoice Items

Retrieves invoice items from EenvoudigFactureren.

```
GET https://connect.mindcloud.co/v1/universal/eenvoudigFactureren/latest/actions/list-invoice-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EenvoudigFactureren `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eenvoudigFactureren/latest/actions/list-invoice-items?connectionId=$CONNECTION_ID&limit=25&offset=0&invoice_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "invoice_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eenvoudigFactureren/latest/actions/list-invoice-items?${params}`, {
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
| `invoice_id` | string | yes | EenvoudigFactureren invoice ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "item_id": 1,
      "price": 1,
      "quantity": 1,
      "total": 1,
      "uri": "string",
      "vat": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `item_id` | number |  |
| `price` | number |  |
| `quantity` | number |  |
| `total` | number |  |
| `uri` | string |  |
| `vat` | number |  |

## Native endpoint

Through the native EenvoudigFactureren API, this operation is `GET /invoices/:invoice_id/items` (base URL `https://eenvoudigfactureren.be/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-invoice-items.md) for the provider-specific parameters and requirements.

