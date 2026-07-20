# CircleCI: Update Schedule



```
PUT https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/update-schedule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CircleCI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/update-schedule" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/update-schedule', {
  method: 'PUT',
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
| `attribution_actor` | string | no | Actor to attribute schedule-triggered pipelines to. |
| `description` | string | no | Schedule description. |
| `name` | string | no | Schedule name. |
| `parameters` | object | no | Pipeline parameters to send when the schedule runs. |
| `schedule_id` | string | no | Opaque schedule identifier. |
| `timetable` | object | no | Schedule timetable definition. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "id": "string",
      "name": "Ava Chen",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `id` | string |  |
| `name` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native CircleCI API, this operation is `PATCH /schedule/:schedule_id` (base URL `https://circleci.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-schedule.md) for the provider-specific parameters and requirements.

