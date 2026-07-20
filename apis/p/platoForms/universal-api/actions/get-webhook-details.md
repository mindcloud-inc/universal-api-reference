# PlatoForms: Get Webhook Details

Retrieves webhook subscription details from PlatoForms.

```
GET https://connect.mindcloud.co/v1/universal/platoForms/latest/actions/get-webhook-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PlatoForms `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/platoForms/latest/actions/get-webhook-details?connectionId=$CONNECTION_ID&web_hooks_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "web_hooks_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/platoForms/latest/actions/get-webhook-details?${params}`, {
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
| `web_hooks_id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "create_shared_urls": true,
      "created_date": "2026-05-07T12:00:00.000Z",
      "form": {},
      "hook_url": "https://example.com",
      "id": "string",
      "is_instant": true,
      "name": "Ava Chen",
      "submit_data_as_dict": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `create_shared_urls` | boolean |  |
| `created_date` | date |  |
| `form` | object |  |
| `hook_url` | string |  |
| `id` | string |  |
| `is_instant` | boolean |  |
| `name` | string |  |
| `submit_data_as_dict` | boolean |  |

## Native endpoint

Through the native PlatoForms API, this operation is `GET /webhooks/{{web_hooks_id}}/` (base URL `https://api.platoforms.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-webhook-details.md) for the provider-specific parameters and requirements.

