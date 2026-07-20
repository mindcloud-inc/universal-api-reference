# Papersign: List Papersign Folder Webhooks



```
GET https://connect.mindcloud.co/v1/universal/papersign/latest/actions/list-papersign-folder-webhooks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Papersign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/papersign/latest/actions/list-papersign-folder-webhooks?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/papersign/latest/actions/list-papersign-folder-webhooks?${params}`, {
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
| `id` | string | yes | The Papersign folder ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "results": {
        "webhooks": {
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
| `results.webhooks.folder.id` | number | The unique identifier of the folder. |
| `results.webhooks.folder.name` | string | The name of the folder. |
| `results.webhooks.id` | number | The unique identifier of the webhook. |
| `results.webhooks.scope` | string | The scope of the webhook. |
| `results.webhooks.target_url` | string | The target URL for the webhook. |
| `results.webhooks.triggers[]` | string | The webhook triggers. |
| `status` | string | Response status. |

## Native endpoint

Through the native Papersign API, this operation is `GET /papersign/folders/:id/webhooks` (base URL `https://api.paperform.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-papersign-folder-webhooks.md) for the provider-specific parameters and requirements.

