# CircleCI: Rollback Project



```
PUT https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/rollback-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CircleCI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/rollback-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/rollback-project', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `component_name` | string | no | Component name to roll back. |
| `current_version` | string | no | Current deployed version. |
| `environment_name` | string | no | Environment name. |
| `namespace` | string | no | Deployment namespace. |
| `parameters` | object | no | Rollback parameters. |
| `project_id` | string | no | Opaque project identifier. |
| `reason` | string | no | Reason for the rollback. |
| `target_version` | string | no | Target rollback version. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "componentName": "Ava Chen",
      "message": "string",
      "projectId": "string",
      "targetVersion": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `componentName` | string |  |
| `message` | string |  |
| `projectId` | string |  |
| `targetVersion` | string |  |

## Native endpoint

Through the native CircleCI API, this operation is `POST /projects/:project_id/rollback` (base URL `https://circleci.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/rollback-project.md) for the provider-specific parameters and requirements.

