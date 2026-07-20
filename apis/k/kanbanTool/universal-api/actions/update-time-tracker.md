# Kanban Tool: Update Time Tracker



```
PUT https://connect.mindcloud.co/v1/universal/kanbanTool/latest/actions/update-time-tracker
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kanban Tool `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/kanbanTool/latest/actions/update-time-tracker" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "timeTrackerId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kanbanTool/latest/actions/update-time-tracker', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "timeTrackerId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `timeTrackerId` | number | yes | Kanban Tool time tracker ID. |
| `startedAt` | date | no | Start timestamp. Example: `2026-03-24T14:30:00.000+00:00`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `position` | number | no | Tracker position on the task. Example: `1`. |
| `listed` | boolean | no | Whether the tracker should be shown in the timers list. |
| `endedAt` | date | no | End timestamp. Example: `2026-03-24T15:00:00.000+00:00`. |
| `highlightedAt` | date | no | Highlight timestamp. Example: `2026-03-24T15:00:00.000+00:00`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "time_tracker": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `time_tracker` | object |  |

## Native endpoint

Through the native Kanban Tool API, this operation is `PUT /time_trackers/:time_tracker_id.json` (base URL `https://{{credentials.domain}}.kanbantool.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-time-tracker.md) for the provider-specific parameters and requirements.

