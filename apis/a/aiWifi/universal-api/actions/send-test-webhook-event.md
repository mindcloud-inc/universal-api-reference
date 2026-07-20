# AiWifi: Send test webhook event

Sends a test event to a webhook in AiWifi.

```
POST https://connect.mindcloud.co/v1/universal/aiWifi/latest/actions/send-test-webhook-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AiWifi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/aiWifi/latest/actions/send-test-webhook-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "webhookId": 1,
  "event": "guest.connected"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aiWifi/latest/actions/send-test-webhook-event', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "webhookId": 1,
    "event": "guest.connected"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `webhookId` | number | yes |  |
| `event` | list<string> | yes | One of: `guest.connected`, `guest.data`, `guest.interests`, `surveyAnswer.created`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attempts": 1,
      "code": 1,
      "endpointUrl": "https://example.com",
      "eventId": "string",
      "eventType": "string",
      "requestSent": {},
      "responseReceived": {},
      "status": "string",
      "timestamp": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attempts` | number |  |
| `code` | number |  |
| `endpointUrl` | string |  |
| `eventId` | string |  |
| `eventType` | string |  |
| `requestSent` | object |  |
| `responseReceived` | object |  |
| `status` | string |  |
| `timestamp` | date |  |

## Native endpoint

Through the native AiWifi API, this operation is `POST /brands/{{brandId}}/webhook-configs/{{webhookId}}/event/test` (base URL `https://api.aiwifi.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-test-webhook-event.md) for the provider-specific parameters and requirements.

