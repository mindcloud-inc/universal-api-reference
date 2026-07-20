# Instantly: Send Test Email

Sends a test email from Instantly.

```
POST https://connect.mindcloud.co/v1/universal/instantly/latest/actions/send-test-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instantly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/instantly/latest/actions/send-test-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "eaccount": "string",
  "toAddressEmailList": "ava@example.com",
  "subject": "string",
  "body": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/instantly/latest/actions/send-test-email', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
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
| `eaccount` | string | yes | Connected email account used to send the test email. |
| `toAddressEmailList` | string | yes | Comma-separated recipient email addresses. |
| `subject` | string | yes | Email subject. |
| `body` | object | yes | Email body object with html and/or text. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "status": "string",
      "subject": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Email ID. |
| `status` | string | Send status. |
| `subject` | string | Subject. |

## Native endpoint

Through the native Instantly API, this operation is `POST /api/v2/emails/test` (base URL `https://api.instantly.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-test-email.md) for the provider-specific parameters and requirements.

