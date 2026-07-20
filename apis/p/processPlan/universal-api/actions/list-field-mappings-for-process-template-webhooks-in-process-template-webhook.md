# Process Plan: List Field Mappings for Process Template Webhooks in Process Template Webhook



```
GET https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/list-field-mappings-for-process-template-webhooks-in-process-template-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Process Plan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/list-field-mappings-for-process-template-webhooks-in-process-template-webhook?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/list-field-mappings-for-process-template-webhooks-in-process-template-webhook?${params}`, {
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
| `processTemplateWebhookId` | string | no | Process template webhook ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Process Plan API returns.

## Native endpoint

Through the native Process Plan API, this operation is `GET /process_template_webhook/:processTemplateWebhookId/process_template_webhook/field_map/list` (base URL `https://apius0.processplan.com/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-field-mappings-for-process-template-webhooks-in-process-template-webhook.md) for the provider-specific parameters and requirements.

