# WhautoChat: List WhatsApp Templates

Retrieves WhatsApp templates from WhautoChat.

```
GET https://connect.mindcloud.co/v1/universal/whautoChat/latest/actions/list-whats-app-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WhautoChat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whautoChat/latest/actions/list-whats-app-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/whautoChat/latest/actions/list-whats-app-templates?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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

Through the native WhautoChat API, this operation is `GET /v1/whatsapp-templates` (base URL `https://api.whauto.chat`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-whats-app-templates.md) for the provider-specific parameters and requirements.

