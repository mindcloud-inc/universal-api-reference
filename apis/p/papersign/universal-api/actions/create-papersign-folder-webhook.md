# Papersign: Create Papersign Folder Webhook



```
POST https://connect.mindcloud.co/v1/universal/papersign/latest/actions/create-papersign-folder-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Papersign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/papersign/latest/actions/create-papersign-folder-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/papersign/latest/actions/create-papersign-folder-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The Papersign folder ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "results": {
        "webhook": {
          "folder": {
            "id": 1,
            "name": "Ava Chen"
          },
          "id": 1,
          "scope": "string",
          "target_url": "https://example.com",
          "triggers": [
            "string"
          ]
        }
      },
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `results.webhook.folder.id` | number | The unique identifier of the folder. |
| `results.webhook.folder.name` | string | The name of the folder. |
| `results.webhook.id` | number | The unique identifier of the webhook. |
| `results.webhook.scope` | string | The scope of the webhook. |
| `results.webhook.target_url` | string | The target URL for the webhook. |
| `results.webhook.triggers[]` | string | The webhook triggers. |
| `status` | string | Response status. |

## Native endpoint

Through the native Papersign API, this operation is `POST /papersign/folders/:id/webhooks` (base URL `https://api.paperform.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-papersign-folder-webhook.md) for the provider-specific parameters and requirements.

