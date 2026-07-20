# CircleCI: List Deploy Component Versions



```
GET https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/list-deploy-component-versions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CircleCI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/list-deploy-component-versions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/list-deploy-component-versions?${params}`, {
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
| `component_id` | string | no | The deploy component ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "environmentId": "string",
      "isLive": true,
      "jobId": "string",
      "jobNumber": 1,
      "lastDeployedAt": "string",
      "name": "Ava Chen",
      "namespace": "Ava Chen",
      "pipelineId": "string",
      "workflowId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `environmentId` | string |  |
| `isLive` | boolean |  |
| `jobId` | string |  |
| `jobNumber` | number |  |
| `lastDeployedAt` | string |  |
| `name` | string |  |
| `namespace` | string |  |
| `pipelineId` | string |  |
| `workflowId` | string |  |

## Native endpoint

Through the native CircleCI API, this operation is `GET /deploy/components/:component_id/versions` (base URL `https://circleci.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-deploy-component-versions.md) for the provider-specific parameters and requirements.

