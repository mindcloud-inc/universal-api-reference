# YouCan: Mark Order As Paid

Updates an order in YouCan by marking it paid.

```
PUT https://connect.mindcloud.co/v1/universal/youCan/latest/actions/mark-order-as-paid
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a YouCan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/youCan/latest/actions/mark-order-as-paid" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/youCan/latest/actions/mark-order-as-paid', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `type` | string |  |

## Native endpoint

Through the native YouCan API, this operation is `PUT /orders/{id}/pay` (base URL `https://api.youcan.shop`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/mark-order-as-paid.md) for the provider-specific parameters and requirements.

