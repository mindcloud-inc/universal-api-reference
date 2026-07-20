# Booqable: Get New Order

Retrieves an existing or new order for the current employee in Booqable.

```
GET https://connect.mindcloud.co/v1/universal/booqable/latest/actions/get-new-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Booqable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/booqable/latest/actions/get-new-order?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/booqable/latest/actions/get-new-order?${params}`, {
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

Through the native Booqable API, this operation is `GET /orders/new` (base URL `https://mindcloud.booqable.com/api/4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-new-order.md) for the provider-specific parameters and requirements.

