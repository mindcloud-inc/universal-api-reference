# Printful: Confirm Order

Confirms a draft Printful order for fulfillment.

```
PUT https://connect.mindcloud.co/v1/universal/printful/latest/actions/confirm-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Printful `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/printful/latest/actions/confirm-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "1"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/printful/latest/actions/confirm-order', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "1"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The Printful order id or external id prefixed with @. Default: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": 1,
      "external_id": "string",
      "id": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | number |  |
| `external_id` | string |  |
| `id` | number |  |
| `status` | string |  |

## Native endpoint

Through the native Printful API, this operation is `POST /orders/{id}/confirm` (base URL `https://api.printful.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/confirm-order.md) for the provider-specific parameters and requirements.

