# SafetyCulture: Update Action Status

Updates an action status in SafetyCulture.

```
PUT https://connect.mindcloud.co/v1/universal/safetyCulture/latest/actions/update-action-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SafetyCulture `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/safetyCulture/latest/actions/update-action-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "taskId": "string",
  "statusId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/safetyCulture/latest/actions/update-action-status', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "taskId": "string",
    "statusId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `taskId` | string | yes | Required. The ID of the action or issue you're updating. |
| `statusId` | string | yes | Required. The ID of the status you're updating the action or issue to. An issue can be in an "Open" or "Resolved" status, where each status is represented by hardcoded UUID values. Issue statuses: - Open: `547ed646-5e34-4732-bb54-a199d304368a`. - Resolved: `450484b1-56cd-4784-9b49-a3cf97d0c0ad`. An action can be in a "To do", "In progress", "Complete", or "Can't do" status, where each status is represented by hardcoded UUID values. Action statuses: - To do: `17e793a1-26a3-4ecd-99ca-f38ecc6eaa2e`. - In progress: `20ce0cb1-387a-47d4-8c34-bc6fd3be0e27`. - Complete: `7223d809-553e-4714-a038-62dc98f3fbf3`. - Can't do: `06308884-41c2-4ee0-9da7-5676647d3d75`. |
| `modifiedAt` | date | no | Optional. The UTC time and date the modification took place. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | object |  |

## Native endpoint

Through the native SafetyCulture API, this operation is `PUT /tasks/v1/actions/{task_id}/status` (base URL `https://api.safetyculture.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-action-status.md) for the provider-specific parameters and requirements.

