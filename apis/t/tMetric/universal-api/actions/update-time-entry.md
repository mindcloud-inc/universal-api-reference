# TMetric: Update Time Entry



```
PUT https://connect.mindcloud.co/v1/universal/tMetric/latest/actions/update-time-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TMetric `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/tMetric/latest/actions/update-time-entry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": 1,
  "timeEntryId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tMetric/latest/actions/update-time-entry', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": 1,
    "timeEntryId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | number | yes | Workspace identifier. |
| `endTime` | date | no | Updated end time. |
| `note` | string | no | Optional time entry note. |
| `project.id` | number | no | Project identifier. |
| `startTime` | date | no | Updated start time. |
| `task.id` | number | no | Existing task identifier. |
| `task.name` | string | no | Task name when targeting a task by name. |
| `timeEntryId` | number | yes | Time entry identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "endTime": "string",
      "id": 1,
      "isBillable": true,
      "isInvoiced": true,
      "note": "string",
      "startTime": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `endTime` | string |  |
| `id` | number |  |
| `isBillable` | boolean |  |
| `isInvoiced` | boolean |  |
| `note` | string |  |
| `startTime` | date |  |

## Native endpoint

Through the native TMetric API, this operation is `PUT /accounts/:accountId/timeentries/:timeEntryId` (base URL `https://app.tmetric.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-time-entry.md) for the provider-specific parameters and requirements.

