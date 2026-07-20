# Port API AI: Get Workflow

Retrieves a workflow from Port.

```
GET https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/get-workflow
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Port API AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/get-workflow?connectionId=$CONNECTION_ID&workflowIdentifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workflowIdentifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/get-workflow?${params}`, {
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
| `workflowIdentifier` | string | yes | The Port workflow identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ok": true,
      "workflow": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ok` | boolean |  |
| `workflow` | object |  |

## Native endpoint

Through the native Port API AI API, this operation is `GET /workflows/:workflow_identifier` (base URL `https://api.port.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-workflow.md) for the provider-specific parameters and requirements.

