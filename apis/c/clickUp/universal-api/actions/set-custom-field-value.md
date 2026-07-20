# ClickUp: Set Custom Field Value

Add data to a Custom field on a task.

```
PUT https://connect.mindcloud.co/v1/universal/clickUp/latest/actions/set-custom-field-value
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClickUp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/clickUp/latest/actions/set-custom-field-value" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "taskId": "string",
  "fieldId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clickUp/latest/actions/set-custom-field-value', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "taskId": "string",
    "fieldId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `taskId` | string | yes |  |
| `fieldId` | string | yes |  |
| `customTaskids` | boolean | no | If you want to reference a task by its Custom Task ID, this value must be true. |
| `teamId` | list | no | When the custom_task_ids parameter is set to true, the Workspace ID must be provided using the team_id parameter. For example: custom_task_ids=true&team_id=123. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ClickUp API returns.

## Native endpoint

Through the native ClickUp API, this operation is `POST task/:task_id/field/:field_id` (base URL `https://api.clickup.com/api/v2/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-custom-field-value.md) for the provider-specific parameters and requirements.

