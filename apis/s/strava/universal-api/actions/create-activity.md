# Strava: Create Activity

Creates a new activity in Strava.

```
POST https://connect.mindcloud.co/v1/universal/strava/latest/actions/create-activity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Strava `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/strava/latest/actions/create-activity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "sportType": "string",
  "startDateLocal": "2026-05-07T12:00:00.000Z",
  "elapsedTime": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/strava/latest/actions/create-activity', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "sportType": "string",
    "startDateLocal": "2026-05-07T12:00:00.000Z",
    "elapsedTime": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | The name of the activity. |
| `sportType` | string | yes | The sport type of the activity. |
| `startDateLocal` | date | yes | The local start date/time for the activity. |
| `elapsedTime` | number | yes | Elapsed time in seconds. |
| `description` | string | no | Description of the activity. |
| `distance` | number | no | Distance in meters. |
| `trainer` | boolean | no | Whether the activity was done on a trainer. |
| `commute` | boolean | no | Whether the activity was a commute. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Strava API returns.

## Native endpoint

Through the native Strava API, this operation is `POST /activities` (base URL `https://www.strava.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-activity.md) for the provider-specific parameters and requirements.

