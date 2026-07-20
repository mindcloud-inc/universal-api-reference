# MailerSend: Get Message



```
GET https://connect.mindcloud.co/v1/universal/mailerSend/latest/actions/get-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailerSend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailerSend/latest/actions/get-message?connectionId=$CONNECTION_ID&messageId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "messageId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailerSend/latest/actions/get-message?${params}`, {
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
| `messageId` | string | yes | ID of the MailerSend message. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "domain": {},
      "emails": [
        {}
      ],
      "id": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string | Message creation timestamp. |
| `domain` | object | Verified sending domain attached to the message. |
| `emails` | array<object> | Email records linked to this message. |
| `id` | string | MailerSend message ID. |
| `updatedAt` | string | Message update timestamp. |

## Native endpoint

Through the native MailerSend API, this operation is `GET /messages/:message_id` (base URL `https://api.mailersend.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-message.md) for the provider-specific parameters and requirements.

