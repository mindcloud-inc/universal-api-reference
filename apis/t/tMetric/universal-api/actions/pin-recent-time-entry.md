# TMetric: Pin Recent Time Entry



```
PUT https://connect.mindcloud.co/v1/universal/tMetric/latest/actions/pin-recent-time-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TMetric `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/tMetric/latest/actions/pin-recent-time-entry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tMetric/latest/actions/pin-recent-time-entry', {
  method: 'PUT',
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
| `isBillable` | boolean | no | Whether the recent entry is billable. |
| `isPinned` | boolean | no | Whether to pin the recent time entry. |
| `note` | string | no | Optional recent-entry note. |
| `project.id` | number | no | Project identifier. |
| `task.id` | number | no | Existing task identifier. |
| `task.name` | string | no | Task name when targeting a task by name. |
| `userId` | number | no | Optional user identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": "string",
      "meta": {
        "curl": "https://example.com",
        "response": {
          "status": 1,
          "statusText": "string"
        }
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | string |  |
| `meta.curl` | string |  |
| `meta.response.status` | number |  |
| `meta.response.statusText` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native TMetric API, this operation is `PUT /accounts/:accountId/timeentries/recent` (base URL `https://app.tmetric.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/pin-recent-time-entry.md) for the provider-specific parameters and requirements.

