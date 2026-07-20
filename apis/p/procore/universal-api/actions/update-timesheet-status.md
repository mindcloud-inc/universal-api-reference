# Procore: Update Timesheet Status

Updates a timesheet approval status in Procore.

```
PUT https://connect.mindcloud.co/v1/universal/procore/latest/actions/update-timesheet-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Procore `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/procore/latest/actions/update-timesheet-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string",
  "timesheets[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/procore/latest/actions/update-timesheet-status', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "string",
    "timesheets[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | string | yes | Unique identifier for the project. |
| `timesheets[]` | array<object> | yes | Timesheet approval update payload array. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Procore API returns.

## Native endpoint

Through the native Procore API, this operation is `PATCH /rest/v1.0/projects/:project_id/timesheets/update_approval` (base URL `https://api.procore.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-timesheet-status.md) for the provider-specific parameters and requirements.

