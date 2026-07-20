# Skyvern: Delete Workflow

Deletes an existing workflow from Skyvern.

```
DELETE https://connect.mindcloud.co/v1/universal/skyvern/latest/actions/delete-workflow
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Skyvern `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/skyvern/latest/actions/delete-workflow?connectionId=$CONNECTION_ID&workflowId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workflowId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/skyvern/latest/actions/delete-workflow?${params}`, {
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
| `workflowId` | string | yes | The ID of the workflow to delete. Workflow ID starts with wpid_. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Skyvern API returns.

## Native endpoint

Through the native Skyvern API, this operation is `POST /v1/workflows/:workflow_id/delete` (base URL `https://api.skyvern.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-workflow.md) for the provider-specific parameters and requirements.

