# Famulor AI - Voice Agent: Enable Assistant Inbound Webhook

Enables inbound webhook notifications for a Famulor assistant.

```
PUT https://connect.mindcloud.co/v1/universal/famulorAIVoiceAgent/latest/actions/enable-assistant-inbound-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Famulor AI - Voice Agent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/famulorAIVoiceAgent/latest/actions/enable-assistant-inbound-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "assistant_id": 1,
  "webhook_url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/famulorAIVoiceAgent/latest/actions/enable-assistant-inbound-webhook', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "assistant_id": 1,
    "webhook_url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `assistant_id` | number | yes | Assistant ID to enable inbound webhooks for. |
| `webhook_url` | string | yes | Endpoint URL that receives inbound webhook notifications. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Webhook configuration details. |
| `message` | string | Result message. |

## Native endpoint

Through the native Famulor AI - Voice Agent API, this operation is `POST /user/assistants/enable-inbound-webhook` (base URL `https://app.famulor.de/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/enable-assistant-inbound-webhook.md) for the provider-specific parameters and requirements.

