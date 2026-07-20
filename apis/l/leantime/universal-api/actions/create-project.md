# Leantime: Create Project



```
POST https://connect.mindcloud.co/v1/universal/leantime/latest/actions/create-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leantime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/leantime/latest/actions/create-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "params.values.name": "Ava Chen",
  "params.values.clientId": "0"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/leantime/latest/actions/create-project', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "params.values.name": "Ava Chen",
    "params.values.clientId": "0"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `params.values.name` | string | yes | The new project name. |
| `params.values.clientId` | number | yes | The client ID for the project. Default: `0`. |
| `params.values.details` | string | no | Additional project details. |
| `params.values.start` | string | no | Project start date in the workspace user format. |
| `params.values.end` | string | no | Project end date in the workspace user format. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `params.values.hourBudget` | number | no | Planned project hours. |
| `params.values.dollarBudget` | number | no | Planned project budget in dollars. |
| `params.values.psettings` | string | no | Project visibility settings. Default: `restricted`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Leantime API returns.

## Native endpoint

Through the native Leantime API, this operation is `POST /` (base URL `{{credentials.workspaceUrl}}/api/jsonrpc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-project.md) for the provider-specific parameters and requirements.

