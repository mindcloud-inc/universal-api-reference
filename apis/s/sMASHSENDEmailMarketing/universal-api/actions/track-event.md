# SMASHSEND Email Marketing: Track Event

Tracks a single contact event in SMASHSEND.

```
POST https://connect.mindcloud.co/v1/universal/sMASHSENDEmailMarketing/latest/actions/track-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SMASHSEND Email Marketing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sMASHSENDEmailMarketing/latest/actions/track-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "event": "string",
  "identify": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sMASHSENDEmailMarketing/latest/actions/track-event', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "event": "string",
    "identify": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `event` | string | yes | Event name to track, for example user.signup or purchase.completed. |
| `identify` | object | yes | Identity payload for the event, including at least the contact email. |
| `messageId` | string | no | Optional custom message ID for deduplication. |
| `properties` | object | no | Optional event properties object. |
| `timestamp` | date | no | Optional ISO 8601 timestamp for the event. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SMASHSEND Email Marketing API returns.

## Native endpoint

Through the native SMASHSEND Email Marketing API, this operation is `POST /v1/events` (base URL `https://api.smashsend.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/track-event.md) for the provider-specific parameters and requirements.

