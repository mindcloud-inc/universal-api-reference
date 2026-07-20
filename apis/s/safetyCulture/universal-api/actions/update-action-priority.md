# SafetyCulture: Update Action Priority

Updates an action priority in SafetyCulture.

```
PUT https://connect.mindcloud.co/v1/universal/safetyCulture/latest/actions/update-action-priority
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SafetyCulture `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/safetyCulture/latest/actions/update-action-priority" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "taskId": "string",
  "priorityId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/safetyCulture/latest/actions/update-action-priority', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "taskId": "string",
    "priorityId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `taskId` | string | yes | Required. The UUID of the task being updated. |
| `priorityId` | string | yes | Required. The new priority UUID for the task. |
| `modifiedAt` | date | no | Optional. The timestamp of when this event occurred. |

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

Through the native SafetyCulture API, this operation is `PUT /tasks/v1/actions/{task_id}/priority` (base URL `https://api.safetyculture.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-action-priority.md) for the provider-specific parameters and requirements.

