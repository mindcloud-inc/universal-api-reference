# Flow App: Create Event



```
POST https://connect.mindcloud.co/v1/universal/flowApp/latest/actions/create-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flow App `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/flowApp/latest/actions/create-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "creatorId": 1,
  "title": "string",
  "description": "string",
  "date": "string",
  "time": "string",
  "timezone": "string",
  "operators[]": [
    {}
  ],
  "operators[].id": 1,
  "operators[].role": 1,
  "operators[].micEnabled": true,
  "operators[].camEnabled": true,
  "operators[].screenSharingEnabled": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/flowApp/latest/actions/create-event', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "creatorId": 1,
    "title": "string",
    "description": "string",
    "date": "string",
    "time": "string",
    "timezone": "string",
    "operators[]": [{}],
    "operators[].id": 1,
    "operators[].role": 1,
    "operators[].micEnabled": true,
    "operators[].camEnabled": true,
    "operators[].screenSharingEnabled": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `published` | boolean | no | Whether to publish the event immediately or save it as a draft. |
| `creatorId` | number | yes | The numeric ID of the event creator. |
| `title` | string | yes | The event title. |
| `description` | string | yes | The event description shown on registration and access pages. |
| `date` | string | yes | The event date in YYYY-MM-DD format. |
| `time` | string | yes | The event time in 24-hour HH:MI:SS format. |
| `timezone` | string | yes | A MomentJS-compatible timezone string. |
| `operators[]` | array<object> | yes | Array of operator objects participating in the event. |
| `operators[].id` | number | yes | Operator ID in the operators array. |
| `operators[].role` | number | yes | Operator role where 5 is presenter and 10 is organizer. |
| `operators[].micEnabled` | boolean | yes | Whether the operator microphone is enabled. |
| `operators[].camEnabled` | boolean | yes | Whether the operator camera is enabled. |
| `operators[].screenSharingEnabled` | boolean | yes | Whether screen sharing is enabled for the operator. |
| `duration` | number | no | Estimated event duration in hours. |
| `earlyAccessPeriod` | number | no | Minutes before the event when attendees can begin logging in. |
| `videoRecord` | boolean | no | Whether the event should be recorded. |
| `onDemandReplays` | boolean | no | Whether attendees can register to view replays after the event ends. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "localDescription": "string",
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number | Provider-level Flow response code returned by the create event endpoint. |
| `localDescription` | string | Provider error description returned by Flow when event creation is rejected. |
| `message` | string | Provider response message returned by the create event endpoint. |

## Native endpoint

Through the native Flow App API, this operation is `POST /event` (base URL `https://prod.flowapp.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-event.md) for the provider-specific parameters and requirements.

