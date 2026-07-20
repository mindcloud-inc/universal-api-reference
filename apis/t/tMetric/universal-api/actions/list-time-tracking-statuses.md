# TMetric: List Time Tracking Statuses



```
GET https://connect.mindcloud.co/v1/universal/tMetric/latest/actions/list-time-tracking-statuses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TMetric `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tMetric/latest/actions/list-time-tracking-statuses?connectionId=$CONNECTION_ID&accountId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tMetric/latest/actions/list-time-tracking-statuses?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | number | yes | Workspace identifier. |
| `teamId` | number | no | Optional team identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activeTimer": {
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
      },
      "startTime": "2026-05-07T12:00:00.000Z",
      "timeZone": {
        "currentOffset": 1,
        "displayName": "Ava Chen",
        "id": "string",
        "summerOffset": 1,
        "winterOffset": 1
      },
      "totalSeconds": 1,
      "user": {
        "iconUrl": "https://example.com",
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
| `activeTimer.endTime` | date |  |
| `activeTimer.id` | number |  |
| `activeTimer.isBillable` | boolean |  |
| `activeTimer.isInvoiced` | boolean |  |
| `activeTimer.note` | string |  |
| `activeTimer.project.iconUrl` | string |  |
| `activeTimer.project.id` | number |  |
| `activeTimer.project.invoiceMethod` | string |  |
| `activeTimer.project.isBillable` | boolean |  |
| `activeTimer.project.name` | string |  |
| `activeTimer.project.status` | string |  |
| `activeTimer.startTime` | date |  |
| `activeTimer.task.id` | number |  |
| `activeTimer.task.name` | string |  |
| `startTime` | date |  |
| `timeZone.currentOffset` | number |  |
| `timeZone.displayName` | string |  |
| `timeZone.id` | string |  |
| `timeZone.summerOffset` | number |  |
| `timeZone.winterOffset` | number |  |
| `totalSeconds` | number |  |
| `user.iconUrl` | string |  |
| `user.id` | number |  |
| `user.name` | string |  |

## Native endpoint

Through the native TMetric API, this operation is `GET /accounts/:accountId/timeentries/statuses` (base URL `https://app.tmetric.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-time-tracking-statuses.md) for the provider-specific parameters and requirements.

