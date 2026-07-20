# Unstructured: Update Workflow Notification Channel

Updates a workflow notification channel in Unstructured.

```
PUT https://connect.mindcloud.co/v1/universal/unstructured/latest/actions/update-workflow-notification-channel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Unstructured `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/unstructured/latest/actions/update-workflow-notification-channel" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workflowId": "string",
  "channelId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/unstructured/latest/actions/update-workflow-notification-channel', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workflowId": "string",
    "channelId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workflowId` | string | yes | Workflow ID. |
| `channelId` | string | yes | Workflow notification channel ID. |
| `url` | string | no | Webhook destination URL. |
| `eventTypes[]` | array<string> | no | Events sent to the channel. |
| `description` | string | no | Notification channel description. |
| `enabled` | boolean | no | Enable or disable the channel. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "channelType": "string",
      "createdAt": "string",
      "description": "string",
      "enabled": true,
      "eventTypes": [
        [
          "string"
        ]
      ],
      "id": "string",
      "updatedAt": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channelType` | string | Notification channel type. |
| `createdAt` | string | Creation timestamp. |
| `description` | string | Notification channel description. |
| `enabled` | boolean | Whether the channel is enabled. |
| `eventTypes[]` | array<string> | Event types delivered to the channel. |
| `id` | string | Notification channel ID. |
| `updatedAt` | string | Last update timestamp. |
| `url` | string | Webhook destination URL. |

## Native endpoint

Through the native Unstructured API, this operation is `PATCH /workflows/:workflow_id/notifications/channels/:channel_id` (base URL `https://platform.unstructuredapp.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-workflow-notification-channel.md) for the provider-specific parameters and requirements.

