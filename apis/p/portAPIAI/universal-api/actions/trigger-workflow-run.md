# Port API AI: Trigger Workflow Run

Creates a workflow run in Port.

```
POST https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/trigger-workflow-run
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Port API AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/trigger-workflow-run" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workflowIdentifier": "string",
  "inputs": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/trigger-workflow-run', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workflowIdentifier": "string",
    "inputs": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workflowIdentifier` | string | yes | The workflow identifier. |
| `inputs` | object | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ok": true,
      "workflowRun": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ok` | boolean |  |
| `workflowRun` | object |  |

## Native endpoint

Through the native Port API AI API, this operation is `POST /workflows/:workflow_identifier/runs` (base URL `https://api.port.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/trigger-workflow-run.md) for the provider-specific parameters and requirements.

