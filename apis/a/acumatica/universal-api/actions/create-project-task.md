# Acumatica: Create Project Task



```
POST https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/create-project-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Acumatica `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/create-project-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "wse": "Default",
  "endpointVersion": "25.200.001",
  "projectId.value": "PR00000019",
  "projectTaskId.value": "L726483"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/create-project-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "wse": "Default",
    "endpointVersion": "25.200.001",
    "projectId.value": "PR00000019",
    "projectTaskId.value": "L726483"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `wse` | string | yes | Example: `Default`. |
| `endpointVersion` | string | yes | Example: `25.200.001`. |
| `projectId` | object | no |  |
| `projectId.value` | string | yes | Example: `PR00000019`. |
| `projectTaskId` | object | no |  |
| `projectTaskId.value` | string | yes | Acumatica community evidence shows this value can fail when it contains a hyphen. Example: `L726483`. |
| `description` | object | no |  |
| `description.value` | string | no | Example: `Implementation phase 1`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `visibilitySettings` | object | no |  |
| `visibilitySettings.gl` | object | no |  |
| `visibilitySettings.gl.value` | boolean | no |  |
| `visibilitySettings.ap` | object | no |  |
| `visibilitySettings.ap.value` | boolean | no |  |
| `visibilitySettings.crm` | object | no |  |
| `visibilitySettings.crm.value` | boolean | no |  |
| `visibilitySettings.expenses` | object | no |  |
| `visibilitySettings.expenses.value` | boolean | no |  |
| `visibilitySettings.in` | object | no |  |
| `visibilitySettings.in.value` | boolean | no |  |
| `visibilitySettings.po` | object | no |  |
| `visibilitySettings.po.value` | boolean | no |  |
| `visibilitySettings.so` | object | no |  |
| `visibilitySettings.so.value` | boolean | no |  |
| `visibilitySettings.timeEntries` | object | no |  |
| `visibilitySettings.timeEntries.value` | boolean | no |  |
| `visibilitySettings.ar` | object | no |  |
| `visibilitySettings.ar.value` | boolean | no |  |
| `visibilitySettings.ca` | object | no |  |
| `visibilitySettings.ca.value` | boolean | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Acumatica API returns.

## Native endpoint

Through the native Acumatica API, this operation is `PUT /entity/:wse/:endpointVersion/ProjectTask` (base URL `{{credentials.uRL}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-project-task.md) for the provider-specific parameters and requirements.

