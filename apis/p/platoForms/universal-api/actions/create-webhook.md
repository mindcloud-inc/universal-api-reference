# PlatoForms: Create Webhook

Creates a new webhook in PlatoForms.

```
POST https://connect.mindcloud.co/v1/universal/platoForms/latest/actions/create-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PlatoForms `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/platoForms/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "form_identifier": "string",
  "hook_url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/platoForms/latest/actions/create-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "form_identifier": "string",
    "hook_url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `form_identifier` | string | yes |  |
| `hook_url` | string | yes | Your webhook endpoint URL |
| `name` | string | no | Descriptive name for the webhook |
| `create_shared_urls` | boolean | no | Include public download URLs |
| `submit_data_as_dict` | boolean | no | Send data as dictionary format |
| `is_instant` | boolean | no | Instant delivery vs batched |

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

Through the native PlatoForms API, this operation is `POST /webhooks/form/{{form_identifier}}/` (base URL `https://api.platoforms.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook.md) for the provider-specific parameters and requirements.

