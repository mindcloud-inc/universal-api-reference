# Wati: Send Template Message

Sends an approved WhatsApp template message through Wati.

```
POST https://connect.mindcloud.co/v1/universal/wati/latest/actions/send-template-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wati `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/wati/latest/actions/send-template-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "whatsappNumber": "string",
  "templateName": "Ava Chen",
  "broadcastName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wati/latest/actions/send-template-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "whatsappNumber": "string",
    "templateName": "Ava Chen",
    "broadcastName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `whatsappNumber` | string | yes | Target recipient phone number. |
| `templateName` | string | yes | Approved Wati template name. |
| `broadcastName` | string | yes | Name for the broadcast record. |
| `parameters[]` | array<object> | no | Template parameter values for the message. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contact": {
        "contactStatus": "string",
        "firstName": "Ava",
        "fullName": "Ava Chen",
        "id": "string",
        "lastUpdated": "2026-05-07T12:00:00.000Z",
        "phone": "string"
      },
      "model": {
        "ids": [
          "string"
        ]
      },
      "phoneNumber": "string",
      "result": true,
      "templateName": "Ava Chen",
      "validWhatsAppNumber": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contact` | object | Resolved contact returned by Wati. |
| `contact.contactStatus` | string | Contact validation status. |
| `contact.firstName` | string | Contact first name. |
| `contact.fullName` | string | Contact full name. |
| `contact.id` | string | Wati contact identifier. |
| `contact.lastUpdated` | date | When the contact record was last updated. |
| `contact.phone` | string | Contact phone number. |
| `model` | object | Model wrapper returned by Wati. |
| `model.ids` | array<string> | Wati IDs associated with the operation. |
| `phoneNumber` | string | WhatsApp number used for the template send. |
| `result` | boolean | Whether Wati accepted the template send. |
| `templateName` | string | Template name that was sent. |
| `validWhatsAppNumber` | boolean | Whether Wati considers the target number valid. |

## Native endpoint

Through the native Wati API, this operation is `POST /api/v1/sendTemplateMessage` (base URL `{{credentials.apiEndpointUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-template-message.md) for the provider-specific parameters and requirements.

