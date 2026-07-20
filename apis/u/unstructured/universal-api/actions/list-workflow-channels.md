# Unstructured: List Workflow Channels

Retrieves workflow notification channels from Unstructured.

```
GET https://connect.mindcloud.co/v1/universal/unstructured/latest/actions/list-workflow-channels
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Unstructured `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/unstructured/latest/actions/list-workflow-channels?connectionId=$CONNECTION_ID&workflowId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workflowId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/unstructured/latest/actions/list-workflow-channels?${params}`, {
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
      "channelType": "string",
      "config": {},
      "createdAt": "string",
      "id": "string",
      "name": "Ava Chen",
      "updatedAt": "string",
      "verified": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channelType` | string | Notification channel type. |
| `config` | object | Channel configuration. |
| `createdAt` | string | Creation timestamp. |
| `id` | string | Channel ID. |
| `name` | string | Channel name. |
| `updatedAt` | string | Last update timestamp. |
| `verified` | boolean | Whether the channel is verified. |

## Native endpoint

Through the native Unstructured API, this operation is `GET /workflows/:workflow_id/notifications/channels` (base URL `https://platform.unstructuredapp.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-workflow-channels.md) for the provider-specific parameters and requirements.

