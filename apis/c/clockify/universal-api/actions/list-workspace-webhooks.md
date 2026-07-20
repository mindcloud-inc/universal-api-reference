# Clockify: List Workspace Webhooks

Lists all workspace webhooks in Clockify.

```
GET https://connect.mindcloud.co/v1/universal/clockify/latest/actions/list-workspace-webhooks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clockify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clockify/latest/actions/list-workspace-webhooks?connectionId=$CONNECTION_ID&workspaceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clockify/latest/actions/list-workspace-webhooks?${params}`, {
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
| `workspaceId` | list<string> | yes |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `type` | list<string> | no | One of: `ADDON`, `SYSTEM`, `USER_CREATED`. Example: `STANDARD`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "webhooks": [
        [
          {}
        ]
      ],
      "workspaceWebhookCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `webhooks[]` | array<object> |  |
| `webhooks[].authToken` | string |  |
| `webhooks[].deliveryEnabled` | boolean |  |
| `webhooks[].enabled` | boolean |  |
| `webhooks[].id` | string |  |
| `webhooks[].name` | string |  |
| `webhooks[].triggerSource[]` | array<string> |  |
| `webhooks[].triggerSourceType` | string |  |
| `webhooks[].url` | string |  |
| `webhooks[].userId` | string |  |
| `webhooks[].webhookEvent` | string |  |
| `webhooks[].workspaceId` | string |  |
| `workspaceWebhookCount` | number |  |

## Native endpoint

Through the native Clockify API, this operation is `GET workspaces/:workspaceId/webhooks` (base URL `https://api.clockify.me/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-workspace-webhooks.md) for the provider-specific parameters and requirements.

