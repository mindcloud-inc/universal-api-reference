# Promptmate.io: Create Webhook



```
POST https://connect.mindcloud.co/v1/universal/promptmateio/latest/actions/create-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Promptmate.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/promptmateio/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "endpointUrl": "https://example.com",
  "webhookName": "Ava Chen",
  "webhookType": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/promptmateio/latest/actions/create-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "endpointUrl": "https://example.com",
    "webhookName": "Ava Chen",
    "webhookType": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `endpointUrl` | string | yes | Destination URL Promptmate should call. |
| `restrictedAppIds[]` | array<string> | no | Optional list of Promptmate app IDs allowed to trigger the webhook. |
| `webhookName` | string | yes | Human-readable name for the webhook. |
| `webhookType` | string | yes | Webhook event type. Promptmate currently documents job webhooks. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `webhookReference` | string | no | Optional caller-defined reference value. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "endpointUrl": "https://example.com",
      "restrictedAppIds": [
        "string"
      ],
      "webhookId": "string",
      "webhookName": "Ava Chen",
      "webhookReference": "string",
      "webhookType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `endpointUrl` | string | Webhook destination URL. |
| `restrictedAppIds` | array<string> | Optional Promptmate app IDs allowed to trigger the webhook. |
| `webhookId` | string | Created Promptmate webhook ID. |
| `webhookName` | string | Created Promptmate webhook name. |
| `webhookReference` | string | Caller-defined webhook reference. |
| `webhookType` | string | Webhook event type. |

## Native endpoint

Through the native Promptmate.io API, this operation is `POST /webhooks` (base URL `https://api.promptmate.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook.md) for the provider-specific parameters and requirements.

