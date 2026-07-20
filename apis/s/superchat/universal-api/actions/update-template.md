# Superchat: Update Template

Updates an existing template in Superchat.

```
PUT https://connect.mindcloud.co/v1/universal/superchat/latest/actions/update-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Superchat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/superchat/latest/actions/update-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "template_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/superchat/latest/actions/update-template', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "template_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `template_id` | string | yes | The unique identifier of the template |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | no | Internal name of the template |
| `folder_id` | string | no | The ID of the folder this template should be save in. |
| `file_ids[]` | array<string> | no |  |

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

Through the native Superchat API, this operation is `PATCH /templates/{template_id}` (base URL `https://api.superchat.com/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-template.md) for the provider-specific parameters and requirements.

