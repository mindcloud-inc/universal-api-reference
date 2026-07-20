# Shuffler: Execute Workflow

Creates a workflow execution in Shuffler.

```
POST https://connect.mindcloud.co/v1/universal/shuffler/latest/actions/execute-workflow
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shuffler `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/shuffler/latest/actions/execute-workflow" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workflowId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shuffler/latest/actions/execute-workflow', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workflowId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `executionArgument` | string | no | Optional execution payload. |
| `start` | string | no | Optional start node. |
| `workflowId` | string | yes | Workflow Id path parameter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authorization": "string",
      "executionId": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authorization` | string |  |
| `executionId` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Shuffler API, this operation is `POST /workflows/{workflowId}/execute` (base URL `https://shuffler.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/execute-workflow.md) for the provider-specific parameters and requirements.

