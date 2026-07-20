# Unstructured: List Workflow Notification Channels

Retrieves workflow notification channels from Unstructured.

```
GET https://connect.mindcloud.co/v1/universal/unstructured/latest/actions/list-workflow-notification-channels
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Unstructured `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/unstructured/latest/actions/list-workflow-notification-channels?connectionId=$CONNECTION_ID&workflowId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workflowId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/unstructured/latest/actions/list-workflow-notification-channels?${params}`, {
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
| `workflowId` | string | yes | Workflow ID. |
| `channelType` | string | no | Filter by channel type. Default: `webhook`. |

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

Through the native Unstructured API, this operation is `GET /workflows/:workflow_id/notifications/channels` (base URL `https://platform.unstructuredapp.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-workflow-notification-channels.md) for the provider-specific parameters and requirements.

