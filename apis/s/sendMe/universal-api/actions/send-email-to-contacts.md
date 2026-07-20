# SendMe: Send Email to Contacts



```
POST https://connect.mindcloud.co/v1/universal/sendMe/latest/actions/send-email-to-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SendMe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sendMe/latest/actions/send-email-to-contacts" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contacts[]": [
    "string"
  ],
  "message": "string",
  "subject": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sendMe/latest/actions/send-email-to-contacts', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contacts[]": ["string"],
    "message": "string",
    "subject": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contacts[]` | array<string> | yes | List of email addresses. Accepts multiple values as an array. |
| `message` | string | yes | Email content. |
| `subject` | string | yes | Email subject. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "channel": "string",
      "messages": [
        {}
      ],
      "queueId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channel` | string |  |
| `messages` | array<object> |  |
| `queueId` | string |  |

## Native endpoint

Through the native SendMe API, this operation is `POST /api/messages/email/contacts` (base URL `https://app.sendme123.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-email-to-contacts.md) for the provider-specific parameters and requirements.

