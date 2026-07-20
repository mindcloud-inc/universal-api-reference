# Sensibot.io: WhatsApp Cloud Template Send Message

Sends a WhatsApp Cloud template message through Sensibot.io.

```
POST https://connect.mindcloud.co/v1/universal/sensibotio/latest/actions/whats-app-cloud-template-send-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sensibot.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sensibotio/latest/actions/whats-app-cloud-template-send-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sensibotio/latest/actions/whats-app-cloud-template-send-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cloudWaNumber` | string | no |  |
| `recipient` | string | no |  |
| `templateLanguage` | string | no |  |
| `templateName` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        [
          {}
        ]
      ],
      "message": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[]` | array<object> |  |
| `message` | string |  |
| `status` | number |  |

## Native endpoint

Through the native Sensibot.io API, this operation is `POST /whatsappcloud/send_template` (base URL `https://api.sensibot.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/whats-app-cloud-template-send-message.md) for the provider-specific parameters and requirements.

