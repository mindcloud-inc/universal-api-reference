# TMetric: Add Time Entry Break



```
POST https://connect.mindcloud.co/v1/universal/tMetric/latest/actions/add-time-entry-break
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TMetric `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tMetric/latest/actions/add-time-entry-break" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tMetric/latest/actions/add-time-entry-break', {
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
| `endTime` | date | no | Break end time. |
| `startTime` | date | no | Break start time. |
| `userId` | number | no | Optional user identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "endTime": "2026-05-07T12:00:00.000Z",
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
| `endTime` | date |  |
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

Through the native TMetric API, this operation is `POST /accounts/:accountId/timeentries/break` (base URL `https://app.tmetric.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-time-entry-break.md) for the provider-specific parameters and requirements.

