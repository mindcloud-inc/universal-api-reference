# Superchat: Get Template

Retrieves a template from Superchat by ID.

```
GET https://connect.mindcloud.co/v1/universal/superchat/latest/actions/get-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Superchat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/superchat/latest/actions/get-template?connectionId=$CONNECTION_ID&template_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "template_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/superchat/latest/actions/get-template?${params}`, {
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
| `template_id` | string | yes | The unique identifier of the template |

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

Through the native Superchat API, this operation is `GET /templates/{template_id}` (base URL `https://api.superchat.com/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-template.md) for the provider-specific parameters and requirements.

