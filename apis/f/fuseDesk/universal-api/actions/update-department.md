# FuseDesk: Update Department

Updates an existing department in FuseDesk.

```
PUT https://connect.mindcloud.co/v1/universal/fuseDesk/latest/actions/update-department
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FuseDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/fuseDesk/latest/actions/update-department" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "departmentId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fuseDesk/latest/actions/update-department', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "departmentId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `allReps` | boolean | no | Whether all reps can access the department. |
| `departmentId` | number | yes | The FuseDesk department ID. |
| `feedbackDelay` | number | no | Delay before sending feedback. |
| `feedbackFrequency` | number | no | Feedback request frequency. |
| `feedbackSample` | number | no | Feedback sample percentage. |
| `feedbackTemplateId` | number | no | Feedback template ID. |
| `replyTemplateId` | number | no | Reply template ID. |
| `repUserIds[]` | array<number> | no | Rep user IDs assigned to the department. |
| `stale` | number | no | Stale threshold in minutes. |
| `staleWarning` | number | no | Stale warning threshold in minutes. |
| `templateCategory` | string | no | Template category label. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native FuseDesk API returns.

## Native endpoint

Through the native FuseDesk API, this operation is `POST /api/v2/departments/:departmentId` (base URL `https://{{credentials.appName}}.fusedesk.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-department.md) for the provider-specific parameters and requirements.

