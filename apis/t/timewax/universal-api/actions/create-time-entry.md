# Timewax: Create Time Entry

Creates a new time entry in Timewax.

```
POST https://connect.mindcloud.co/v1/universal/timewax/latest/actions/create-time-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timewax `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/timewax/latest/actions/create-time-entry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "request.timelines.timeline.resource": "string",
  "request.timelines.timeline.project": "string",
  "request.timelines.timeline.breakdown": "string",
  "request.timelines.timeline.date": "2026-05-07T12:00:00.000Z",
  "request.timelines.timeline.hours": 1,
  "request.timelines.timeline.startTime": "string",
  "request.timelines.timeline.endTime": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/timewax/latest/actions/create-time-entry', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "request.timelines.timeline.resource": "string",
    "request.timelines.timeline.project": "string",
    "request.timelines.timeline.breakdown": "string",
    "request.timelines.timeline.date": "2026-05-07T12:00:00.000Z",
    "request.timelines.timeline.hours": 1,
    "request.timelines.timeline.startTime": "string",
    "request.timelines.timeline.endTime": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `request.timelines.timeline.resource` | string | yes | Required. Code or name of the resource. |
| `request.timelines.timeline.project` | string | yes | Required. Code or name of the project. |
| `request.timelines.timeline.breakdown` | string | yes | Required. Code or name of the activity. |
| `request.timelines.timeline.date` | date | yes | Required. Date of the booking, format yyyymmdd or yyyy-mm-dd. |
| `request.timelines.timeline.hours` | number | yes | Required. Number of hours. |
| `request.timelines.timeline.startTime` | string | yes | Required. Start time of the time line, format hh:mm. |
| `request.timelines.timeline.endTime` | string | yes | Required. End time of the time line, format hh:mm. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "valid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `valid` | string | Operation validity indicator. |

## Native endpoint

Through the native Timewax API, this operation is `POST time/entries/add/` (base URL `https://api.timewax.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-time-entry.md) for the provider-specific parameters and requirements.

