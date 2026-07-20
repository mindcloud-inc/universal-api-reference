# GanttPRO: Create Project Custom Day

Creates a custom day in a GanttPRO project calendar.

```
POST https://connect.mindcloud.co/v1/universal/ganttPRO/latest/actions/create-project-custom-day
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GanttPRO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ganttPRO/latest/actions/create-project-custom-day" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": 1,
  "from": "YYYY-MM-DD"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ganttPRO/latest/actions/create-project-custom-day', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": 1,
    "from": "YYYY-MM-DD"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | number | yes | Project identifier for the custom day. |
| `from` | string | yes | Start date in YYYY-MM-DD format. Example: `YYYY-MM-DD`. |
| `to` | string | no | End date in YYYY-MM-DD format. Example: `YYYY-MM-DD`. |
| `title` | string | no | Custom day title. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "from": "2026-05-07T12:00:00.000Z",
      "hours": [
        {}
      ],
      "id": 1,
      "isDayOff": true,
      "repeat": "string",
      "repeatTo": "2026-05-07T12:00:00.000Z",
      "title": "string",
      "to": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `from` | date |  |
| `hours` | array<object> |  |
| `id` | number |  |
| `isDayOff` | boolean |  |
| `repeat` | string |  |
| `repeatTo` | date |  |
| `title` | string |  |
| `to` | date |  |

## Native endpoint

Through the native GanttPRO API, this operation is `POST /projects/customday` (base URL `https://api.ganttpro.com/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-project-custom-day.md) for the provider-specific parameters and requirements.

