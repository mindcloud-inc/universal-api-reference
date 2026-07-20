# TMetric: Create Time Entry



```
POST https://connect.mindcloud.co/v1/universal/tMetric/latest/actions/create-time-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TMetric `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tMetric/latest/actions/create-time-entry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tMetric/latest/actions/create-time-entry', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | number | yes | Workspace identifier. |
| `endTime` | date | no | End time for the time entry. |
| `isBillable` | boolean | no | Whether the time entry is billable. |
| `note` | string | no | Optional time entry note. |
| `project.id` | number | no | Project identifier. |
| `startTime` | date | no | Start time for the time entry. |
| `task.id` | number | no | Existing task identifier. |
| `task.name` | string | no | Task name when creating or targeting a task by name. |
| `userId` | number | no | Optional user identifier. |

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
      "project": {
        "iconUrl": "https://example.com",
        "id": 1,
        "invoiceMethod": "string",
        "isBillable": true,
        "name": "Ava Chen",
        "status": "string"
      },
      "startTime": "2026-05-07T12:00:00.000Z",
      "task": {
        "id": 1,
        "name": "Ava Chen"
      }
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
| `project.iconUrl` | string |  |
| `project.id` | number |  |
| `project.invoiceMethod` | string |  |
| `project.isBillable` | boolean |  |
| `project.name` | string |  |
| `project.status` | string |  |
| `startTime` | date |  |
| `task.id` | number |  |
| `task.name` | string |  |

## Native endpoint

Through the native TMetric API, this operation is `POST /accounts/:accountId/timeentries` (base URL `https://app.tmetric.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-time-entry.md) for the provider-specific parameters and requirements.

