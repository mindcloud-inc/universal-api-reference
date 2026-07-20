# Timing: Start Timer

Starts a new timer in Timing, stopping any running timer.

```
POST https://connect.mindcloud.co/v1/universal/timing/latest/actions/start-timer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/timing/latest/actions/start-timer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/timing/latest/actions/start-timer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `project` | string | no |  |
| `title` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "billingStatus": "string",
      "creatorId": "string",
      "creatorName": "Ava Chen",
      "customFields": {},
      "duration": 1,
      "endDate": "2026-05-07T12:00:00.000Z",
      "isRunning": true,
      "notes": "string",
      "project": {
        "self": "string"
      },
      "self": "string",
      "startDate": "2026-05-07T12:00:00.000Z",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billingStatus` | string |  |
| `creatorId` | string |  |
| `creatorName` | string |  |
| `customFields` | object |  |
| `duration` | number |  |
| `endDate` | date |  |
| `isRunning` | boolean |  |
| `notes` | string |  |
| `project` | object |  |
| `project.self` | string |  |
| `self` | string |  |
| `startDate` | date |  |
| `title` | string |  |

## Native endpoint

Through the native Timing API, this operation is `POST /time-entries/start` (base URL `https://web.timingapp.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/start-timer.md) for the provider-specific parameters and requirements.

