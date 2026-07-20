# Instantly: Reply To Email

Replies to an email in Instantly.

```
POST https://connect.mindcloud.co/v1/universal/instantly/latest/actions/reply-to-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instantly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/instantly/latest/actions/reply-to-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "replyToUuid": "string",
  "eaccount": "string",
  "subject": "string",
  "body": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/instantly/latest/actions/reply-to-email', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "replyToUuid": "string",
    "eaccount": "string",
    "subject": "string",
    "body": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `replyToUuid` | string | yes | ID of the existing email to reply to. |
| `eaccount` | string | yes | Connected email account used to send the reply. |
| `subject` | string | yes | Email subject. |
| `body` | object | yes | Email body object with html and/or text. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "eaccount": "ava@example.com",
      "id": "string",
      "subject": "string",
      "thread_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `eaccount` | string | Sending account. |
| `id` | string | Email ID. |
| `subject` | string | Subject. |
| `thread_id` | string | Thread ID. |

## Native endpoint

Through the native Instantly API, this operation is `POST /api/v2/emails/reply` (base URL `https://api.instantly.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/reply-to-email.md) for the provider-specific parameters and requirements.

