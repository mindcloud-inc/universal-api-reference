# WhatsBox: Send Template Message

Sends an approved template message from WhatsBox.

```
POST https://connect.mindcloud.co/v1/universal/whatsBox/latest/actions/send-template-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WhatsBox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/whatsBox/latest/actions/send-template-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "channelId": "string",
  "to": "string",
  "templateName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/whatsBox/latest/actions/send-template-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "channelId": "string",
    "to": "string",
    "templateName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `channelId` | string | yes | Channel ID for your WhatsApp number. |
| `to` | string | yes | Recipient phone number. |
| `name` | string | no | Recipient name when creating a new contact. |
| `userId` | string | no | Team member ID to show as sender. |
| `medium` | string | no | Platform or application name. |
| `templateName` | string | yes | Approved WhatsApp template name. |
| `components[]` | array<object> | no | Template component parameters. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |

## Native endpoint

Through the native WhatsBox API, this operation is `POST /messages/template` (base URL `https://api.whatsbox.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-template-message.md) for the provider-specific parameters and requirements.

