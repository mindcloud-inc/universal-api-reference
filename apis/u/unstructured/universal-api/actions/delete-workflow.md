# Unstructured: Delete Workflow

Deletes a workflow from Unstructured.

```
DELETE https://connect.mindcloud.co/v1/universal/unstructured/latest/actions/delete-workflow
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Unstructured `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/unstructured/latest/actions/delete-workflow?connectionId=$CONNECTION_ID&workflowId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workflowId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/unstructured/latest/actions/delete-workflow?${params}`, {
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
| `workflowId` | string | yes | The workflow ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Workflow ID. |
| `message` | string | Deletion result message. |
| `status` | string | Deletion status. |

## Native endpoint

Through the native Unstructured API, this operation is `DELETE /workflows/:workflow_id` (base URL `https://platform.unstructuredapp.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-workflow.md) for the provider-specific parameters and requirements.

