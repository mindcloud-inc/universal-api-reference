# Superchat: Create Template

Creates a new template in Superchat.

```
POST https://connect.mindcloud.co/v1/universal/superchat/latest/actions/create-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Superchat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/superchat/latest/actions/create-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/superchat/latest/actions/create-template', {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | no | Internal name of the template |
| `folder_id` | string | no | The ID of the folder this template should be save in. |
| `content` | object | no |  |
| `whats_app_business_account_id` | string | no | The WhatsApp business account on which the template should be created. Required for WhatsApp templates. Starts with `waba_` Get the ID from the /channels or /channels/{channel_id} endpoint. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "channels": {
        "id": "string",
        "name": "Ava Chen",
        "url": "https://example.com"
      },
      "content": {},
      "created_at": "string",
      "folder_id": "string",
      "id": "string",
      "name": "Ava Chen",
      "status": "string",
      "updated_at": "string",
      "url": "https://example.com",
      "whats_app_business_account_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channels` | array<object> |  |
| `channels.id` | string |  |
| `channels.name` | string |  |
| `channels.url` | string |  |
| `content` | object |  |
| `created_at` | string |  |
| `folder_id` | string |  |
| `id` | string |  |
| `name` | string |  |
| `status` | string |  |
| `updated_at` | string |  |
| `url` | string |  |
| `whats_app_business_account_id` | string |  |

## Native endpoint

Through the native Superchat API, this operation is `POST /templates` (base URL `https://api.superchat.com/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-template.md) for the provider-specific parameters and requirements.

