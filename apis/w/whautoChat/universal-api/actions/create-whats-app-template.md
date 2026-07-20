# WhautoChat: Create WhatsApp Template

Creates a new WhatsApp template in WhautoChat.

```
POST https://connect.mindcloud.co/v1/universal/whautoChat/latest/actions/create-whats-app-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WhautoChat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/whautoChat/latest/actions/create-whats-app-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/whautoChat/latest/actions/create-whats-app-template', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `template.category` | string | no |  |
| `template.language` | string | no |  |
| `template.name` | string | no |  |
| `template.components[]` | array<object> | no |  |
| `workspace.id` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "id": "string",
      "template": {
        "category": "string",
        "components": [
          {}
        ],
        "language": "string",
        "name": "Ava Chen",
        "status": "string"
      },
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "workspace": {
        "id": "string",
        "title": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `id` | string |  |
| `template.category` | string |  |
| `template.components` | array<object> |  |
| `template.language` | string |  |
| `template.name` | string |  |
| `template.status` | string |  |
| `updatedAt` | date |  |
| `workspace.id` | string |  |
| `workspace.title` | string |  |

## Native endpoint

Through the native WhautoChat API, this operation is `POST /v1/whatsapp-template` (base URL `https://api.whauto.chat`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-whats-app-template.md) for the provider-specific parameters and requirements.

