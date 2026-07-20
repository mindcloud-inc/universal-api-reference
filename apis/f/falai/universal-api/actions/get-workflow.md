# fal.ai: Get Workflow

Retrieves detailed workflow information from fal.ai.

```
GET https://connect.mindcloud.co/v1/universal/falai/latest/actions/get-workflow
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a fal.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/falai/latest/actions/get-workflow?connectionId=$CONNECTION_ID&username=Ava%20Chen&workflowName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "username": "Ava Chen",
  "workflowName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/falai/latest/actions/get-workflow?${params}`, {
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
| `username` | string | yes | fal.ai username that owns the workflow. |
| `workflowName` | string | yes | Workflow slug or name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "workflow": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `workflow` | object |  |

## Native endpoint

Through the native fal.ai API, this operation is `GET /workflows/:username/:workflowName` (base URL `https://api.fal.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-workflow.md) for the provider-specific parameters and requirements.

