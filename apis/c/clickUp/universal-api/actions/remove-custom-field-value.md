# ClickUp: Remove Custom Field Value

Remove data from a Custom field on a task.

```
DELETE https://connect.mindcloud.co/v1/universal/clickUp/latest/actions/remove-custom-field-value
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClickUp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/clickUp/latest/actions/remove-custom-field-value?connectionId=$CONNECTION_ID&taskId=string&fieldId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskId": "string",
  "fieldId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clickUp/latest/actions/remove-custom-field-value?${params}`, {
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
| `taskId` | string | yes |  |
| `fieldId` | string | yes |  |
| `customTaskids` | boolean | no | If you want to reference a task by its Custom Task ID, this value must be true. |
| `teamId` | number | no | When the custom_task_ids parameter is set to true, the Workspace ID must be provided using the team_id parameter. For example: custom_task_ids=true&team_id=123. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Empty object response on success. |

## Native endpoint

Through the native ClickUp API, this operation is `DELETE task/:task_id/field/:field_id` (base URL `https://api.clickup.com/api/v2/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-custom-field-value.md) for the provider-specific parameters and requirements.

