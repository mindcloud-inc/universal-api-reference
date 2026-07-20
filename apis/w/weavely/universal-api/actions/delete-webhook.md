# Weavely: Delete Webhook

Deletes a webhook from a Weavely form.

```
DELETE https://connect.mindcloud.co/v1/universal/weavely/latest/actions/delete-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Weavely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/weavely/latest/actions/delete-webhook?connectionId=$CONNECTION_ID&formId=string&webhookId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "formId": "string",
  "webhookId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/weavely/latest/actions/delete-webhook?${params}`, {
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
| `formId` | string | yes | The ID of the form where the webhook is registered. |
| `webhookId` | string | yes | The ID of the webhook to delete. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Weavely API returns.

## Native endpoint

Through the native Weavely API, this operation is `DELETE /forms/:formId/webhooks/:webhookId` (base URL `https://api.weavely.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-webhook.md) for the provider-specific parameters and requirements.

