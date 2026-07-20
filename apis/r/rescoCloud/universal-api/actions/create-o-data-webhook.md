# Resco Cloud: Create OData Webhook

Creates an OData webhook in Resco Cloud.

```
POST https://connect.mindcloud.co/v1/universal/rescoCloud/latest/actions/create-o-data-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Resco Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rescoCloud/latest/actions/create-o-data-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "entity": "string",
  "action": "string",
  "rawBody": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rescoCloud/latest/actions/create-o-data-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "entity": "string",
    "action": "string",
    "rawBody": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `entity` | string | yes | Entity name for the webhook subscription. |
| `action` | string | yes | Webhook action: Create, Update, or Delete. |
| `rawBody` | string | yes | JSON webhook body. Example: {"Url":{"CallbackUrl":"https://example.com/webhook"}}. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Resco Cloud API returns.

## Native endpoint

Through the native Resco Cloud API, this operation is `POST https://{{credentials.organization}}.rescocrm.com/odata/v4/$hook` (base URL `https://{{credentials.organization}}.app.resco.net/rest/v1/data`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-o-data-webhook.md) for the provider-specific parameters and requirements.

