# Trust: Remove Testimonial From Widget

Removes a testimonial from a Trust widget.

```
PUT https://connect.mindcloud.co/v1/universal/trust/latest/actions/remove-testimonial-from-widget
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Trust `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/trust/latest/actions/remove-testimonial-from-widget" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "widgetId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/trust/latest/actions/remove-testimonial-from-widget', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "widgetId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The testimonial ID. |
| `widgetId` | string | yes | The widget ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "widgetId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `widgetId` | string |  |

## Native endpoint

Through the native Trust API, this operation is `PUT /testimonial/:id/remove-widget/:widgetId` (base URL `https://api.usetrust.app/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-testimonial-from-widget.md) for the provider-specific parameters and requirements.

