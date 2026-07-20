# Wooxy: Create Event

Creates a new event in Wooxy.

```
POST https://connect.mindcloud.co/v1/universal/wooxy/latest/actions/create-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wooxy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/wooxy/latest/actions/create-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Stage3Purchase20260408"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wooxy/latest/actions/create-event', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Stage3Purchase20260408"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | The unique event name. Use only letters and numbers, up to 40 characters. Example: `Stage3Purchase20260408`. |
| `description` | string | no | Optional description for the event. Example: `Stage 3 test event`. |
| `isConversion` | boolean | no | Whether Wooxy should treat the event as a conversion. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cost.value` | number | no | Optional event cost value. Example: `2.05`. |
| `cost.currency` | string | no | Optional event cost currency (USD or EUR). Example: `USD`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "result": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `result` | boolean |  |

## Native endpoint

Through the native Wooxy API, this operation is `POST v3/custom-event/create` (base URL `https://api.wooxy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-event.md) for the provider-specific parameters and requirements.

