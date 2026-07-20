# Unstructured: Create Workflow Channel

Creates a workflow notification channel in Unstructured.

```
POST https://connect.mindcloud.co/v1/universal/unstructured/latest/actions/create-workflow-channel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Unstructured `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/unstructured/latest/actions/create-workflow-channel" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workflowId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/unstructured/latest/actions/create-workflow-channel', {
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

Through the native Unstructured API, this operation is `POST /workflows/:workflow_id/notifications/channels` (base URL `https://platform.unstructuredapp.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-workflow-channel.md) for the provider-specific parameters and requirements.

