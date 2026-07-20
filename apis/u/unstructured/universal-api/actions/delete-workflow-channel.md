# Unstructured: Delete Workflow Channel

Deletes a workflow notification channel from Unstructured.

```
DELETE https://connect.mindcloud.co/v1/universal/unstructured/latest/actions/delete-workflow-channel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Unstructured `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/unstructured/latest/actions/delete-workflow-channel?connectionId=$CONNECTION_ID&channelId=string&workflowId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "channelId": "string",
  "workflowId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/unstructured/latest/actions/delete-workflow-channel?${params}`, {
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
| `channelId` | string | yes | The workflow channel ID. |
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
| `id` | string | Channel ID. |
| `message` | string | Deletion result message. |
| `status` | string | Deletion status. |

## Native endpoint

Through the native Unstructured API, this operation is `DELETE /workflows/:workflow_id/notifications/channels/:channel_id` (base URL `https://platform.unstructuredapp.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-workflow-channel.md) for the provider-specific parameters and requirements.

