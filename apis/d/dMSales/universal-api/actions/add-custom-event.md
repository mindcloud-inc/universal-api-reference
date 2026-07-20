# DMSales: Add Custom Event

Creates a custom event in DMSales.

```
POST https://connect.mindcloud.co/v1/universal/dMSales/latest/actions/add-custom-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DMSales `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dMSales/latest/actions/add-custom-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "type": "mindcloud_test_event",
  "custom": {
    "source": "mindcloud",
    "purpose": "wizard-validation"
  }
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dMSales/latest/actions/add-custom-event', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "type": "mindcloud_test_event",
    "custom": {"source":"mindcloud","purpose":"wizard-validation"}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `type` | string | yes | Custom event type. Default: `mindcloud_test_event`. |
| `baseKey` | string | no | Optional contact base key. |
| `email` | string | no | Optional contact email. |
| `custom` | object | yes | Custom event payload object. Default: `{"source":"mindcloud","purpose":"wizard-validation"}`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `message` | string |  |

## Native endpoint

Through the native DMSales API, this operation is `POST /api/events/add-custom-event` (base URL `https://app.dmsales.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-custom-event.md) for the provider-specific parameters and requirements.

