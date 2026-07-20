# Kadoa: Create Notification Settings



```
POST https://connect.mindcloud.co/v1/universal/kadoa/latest/actions/create-notification-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kadoa `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/kadoa/latest/actions/create-notification-settings" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "eventType": "workflow_finished"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kadoa/latest/actions/create-notification-settings', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "eventType": "workflow_finished"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `channelIds` | list<string> | no | JSON array of channel IDs Accepts multiple values as an array. |
| `enabled` | boolean | no | Enable notifications Default: `true`. |
| `eventType` | string | yes | Event type Default: `workflow_finished`. |
| `workflowId` | string | no | Workflow ID (omit for workspace-level) |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `eventConfiguration` | object | no | JSON event config |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "settings": {
          "channels": [
            {}
          ],
          "createdAt": "2026-05-07T12:00:00.000Z",
          "enabled": true,
          "eventConfiguration": {},
          "eventType": "string",
          "id": "string",
          "updatedAt": "2026-05-07T12:00:00.000Z",
          "workflowId": "string"
        }
      },
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
| `data.settings.channels` | array<object> |  |
| `data.settings.createdAt` | date |  |
| `data.settings.enabled` | boolean |  |
| `data.settings.eventConfiguration` | object |  |
| `data.settings.eventType` | string |  |
| `data.settings.id` | string |  |
| `data.settings.updatedAt` | date |  |
| `data.settings.workflowId` | string |  |
| `message` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Kadoa API, this operation is `POST /v5/notifications/settings` (base URL `https://api.kadoa.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-notification-settings.md) for the provider-specific parameters and requirements.

