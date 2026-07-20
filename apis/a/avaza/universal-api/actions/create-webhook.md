# Avaza: Create Webhook

Creates a new webhook in Avaza.

```
POST https://connect.mindcloud.co/v1/universal/avaza/latest/actions/create-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Avaza `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/avaza/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "targetUrl": "https://example.com",
  "event": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/avaza/latest/actions/create-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "targetUrl": "https://example.com",
    "event": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `targetUrl` | string | yes | The URL that should be notified of the event. |
| `event` | string | yes | The event code to be notified about. Possible values: company_created, company_deleted, company_updated, contact_created, contact_deleted, contact_updated, invoice_created, invoice_sent, invoice_updated, invoice_deleted, project_created, project_deleted, project_updated, task_created, task_updated, task_deleted, timesheet_created, timesheet_deleted, timesheet_updated, bill_created, bill_updated, estimate_created, estimate_updated, estimate_deleted |
| `secret` | string | no | Optional Secret string (255 char max). If provided, the secret will be BASE 64 encoded and used as a basic authentication http header with webhook notifications. i.e. Authorization Basic [BASE64 of Secret]" |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Avaza API returns.

## Native endpoint

Through the native Avaza API, this operation is `POST /api/Webhook` (base URL `https://api.avaza.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook.md) for the provider-specific parameters and requirements.

