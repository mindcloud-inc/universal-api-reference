# PostcardMania: Bulk Cancel Orders

Cancels existing orders in PostcardMania in bulk.

```
DELETE https://connect.mindcloud.co/v1/universal/postcardMania/latest/actions/bulk-cancel-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PostcardMania `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/postcardMania/latest/actions/bulk-cancel-orders?connectionId=$CONNECTION_ID&orders=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "orders": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/postcardMania/latest/actions/bulk-cancel-orders?${params}`, {
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
| `orders` | list<number> | yes | Array of PostcardMania order IDs to cancel in bulk. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "results": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `results` | array<object> | Per-order bulk cancel results. |

## Native endpoint

Through the native PostcardMania API, this operation is `POST /order/bulk-cancel` (base URL `https://v3.pcmintegrations.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-cancel-orders.md) for the provider-specific parameters and requirements.

