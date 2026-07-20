# Instantly: Forward Email

Forwards an email in Instantly.

```
POST https://connect.mindcloud.co/v1/universal/instantly/latest/actions/forward-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instantly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/instantly/latest/actions/forward-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "replyToUuid": "string",
  "eaccount": "string",
  "toAddressEmailList": "ava@example.com",
  "subject": "string",
  "body": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/instantly/latest/actions/forward-email', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "replyToUuid": "string",
    "eaccount": "string",
    "toAddressEmailList": "ava@example.com",
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
| `replyToUuid` | string | yes | ID of the existing email to forward. |
| `eaccount` | string | yes | Connected email account used to forward the email. |
| `toAddressEmailList` | string | yes | Comma-separated forward recipient email addresses. |
| `subject` | string | yes | Forward email subject. |
| `body` | object | yes | Forward email body object with html and/or text. |

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

Through the native Instantly API, this operation is `POST /api/v2/emails/forward` (base URL `https://api.instantly.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/forward-email.md) for the provider-specific parameters and requirements.

