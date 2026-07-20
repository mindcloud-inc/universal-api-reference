# MailerSend: Get Recipient



```
GET https://connect.mindcloud.co/v1/universal/mailerSend/latest/actions/get-recipient
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailerSend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailerSend/latest/actions/get-recipient?connectionId=$CONNECTION_ID&recipientId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "recipientId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailerSend/latest/actions/get-recipient?${params}`, {
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
| `recipientId` | string | yes | ID of the MailerSend recipient. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "deletedAt": "string",
      "domain": {},
      "email": "ava@example.com",
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
| `createdAt` | string | Recipient creation timestamp. |
| `deletedAt` | string | Recipient deletion timestamp when present. |
| `domain` | object | Verified domain metadata attached to the recipient. |
| `email` | string | Recipient email address. |
| `emails` | array<object> | Email records linked to the recipient. |
| `id` | string | MailerSend recipient ID. |
| `updatedAt` | string | Recipient update timestamp. |

## Native endpoint

Through the native MailerSend API, this operation is `GET /recipients/:recipient_id` (base URL `https://api.mailersend.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-recipient.md) for the provider-specific parameters and requirements.

