# Papersign: Delete Papersign Folder Webhook



```
DELETE https://connect.mindcloud.co/v1/universal/papersign/latest/actions/delete-papersign-folder-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Papersign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/papersign/latest/actions/delete-papersign-folder-webhook?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/papersign/latest/actions/delete-papersign-folder-webhook?${params}`, {
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
| `id` | string | yes | The Papersign webhook ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string | Response status. |

## Native endpoint

Through the native Papersign API, this operation is `DELETE /papersign/webhooks/:id` (base URL `https://api.paperform.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-papersign-folder-webhook.md) for the provider-specific parameters and requirements.

