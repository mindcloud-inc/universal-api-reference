# Evalumo: Subscribe To Export Webhook

Creates an export webhook subscription in Evalumo.

```
POST https://connect.mindcloud.co/v1/universal/evalumo/latest/actions/subscribe-to-export-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Evalumo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/evalumo/latest/actions/subscribe-to-export-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "hookUrl": "https://example.com",
  "hookId": "string",
  "hookName": "Ava Chen",
  "triggerKey": "new_exported_project"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/evalumo/latest/actions/subscribe-to-export-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "hookUrl": "https://example.com",
    "hookId": "string",
    "hookName": "Ava Chen",
    "triggerKey": "new_exported_project"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `hookUrl` | string | yes | Destination URL that will receive export webhook POST requests. |
| `hookId` | string | yes | Unique identifier for this webhook registration. |
| `hookName` | string | yes | Human-readable webhook subscription name. |
| `zapIcon` | string | no | Optional icon slug shown in Evalumo's webhook registration. |
| `triggerKey` | string | yes | Webhook event key, for example new_exported_project. Default: `new_exported_project`. |
| `lineItemsToExpand` | string | no | Optional comma-separated line item sections to include in webhook payloads. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "hookId": "string",
      "hookUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `hookId` | string | Identifier of the registered webhook. |
| `hookUrl` | string | Webhook destination URL stored by Evalumo. |

## Native endpoint

Through the native Evalumo API, this operation is `POST /hook` (base URL `https://api.evalumo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/subscribe-to-export-webhook.md) for the provider-specific parameters and requirements.

