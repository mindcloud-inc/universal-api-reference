# Wooxy: Update Event

Updates an existing event in Wooxy.

```
PUT https://connect.mindcloud.co/v1/universal/wooxy/latest/actions/update-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wooxy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/wooxy/latest/actions/update-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customEvent": "69d68d2a363c31463001917d",
  "name": "Stage3PurchaseUpdated20260408"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wooxy/latest/actions/update-event', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customEvent": "69d68d2a363c31463001917d",
    "name": "Stage3PurchaseUpdated20260408"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customEvent` | string | yes | The existing event ID or event name. Example: `69d68d2a363c31463001917d`. |
| `name` | string | yes | The new unique event name. Use only letters and numbers, up to 40 characters. Example: `Stage3PurchaseUpdated20260408`. |
| `description` | string | no | Optional updated description. Example: `Stage 3 updated event`. |
| `isConversion` | boolean | no | Whether Wooxy should treat the event as a conversion. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cost.value` | number | no | Optional updated cost value. Example: `2.05`. |
| `cost.currency` | string | no | Optional updated cost currency (USD or EUR). Example: `USD`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | boolean |  |

## Native endpoint

Through the native Wooxy API, this operation is `POST v3/custom-event/update` (base URL `https://api.wooxy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-event.md) for the provider-specific parameters and requirements.

