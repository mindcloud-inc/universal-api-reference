# Booqable: Get Order

Retrieves an order from Booqable.

```
GET https://connect.mindcloud.co/v1/universal/booqable/latest/actions/get-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Booqable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/booqable/latest/actions/get-order?connectionId=$CONNECTION_ID&id=2e98315c-3f90-450a-b5b0-955bfb29e2eb" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "2e98315c-3f90-450a-b5b0-955bfb29e2eb"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/booqable/latest/actions/get-order?${params}`, {
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
| `id` | string | yes | The UUID of the order to fetch. Example: `2e98315c-3f90-450a-b5b0-955bfb29e2eb`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fields.orders` | string | no | Comma-separated order fields to include instead of the default fields. Example: `created_at,updated_at,number`. |
| `include` | string | no | Comma-separated relationships to sideload. Example: `barcode,coupon,customer`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {},
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
| `attributes` | object | Order attributes object. |
| `id` | string | Order UUID. |
| `relationships` | object | Order relationships object. |
| `type` | string | Resource type. |

## Native endpoint

Through the native Booqable API, this operation is `GET /orders/:id` (base URL `https://mindcloud.booqable.com/api/4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-order.md) for the provider-specific parameters and requirements.

