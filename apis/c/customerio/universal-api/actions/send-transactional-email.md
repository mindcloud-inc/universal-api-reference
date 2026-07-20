# Customer.io: Send Transactional Email

Sends a transactional email from Customer.io.

```
POST https://connect.mindcloud.co/v1/universal/customerio/latest/actions/send-transactional-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Customer.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/customerio/latest/actions/send-transactional-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "transactionalMessageId": "password-reset",
  "identifiers": {},
  "to": "user@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/customerio/latest/actions/send-transactional-email', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "transactionalMessageId": "password-reset",
    "identifiers": {},
    "to": "user@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `transactionalMessageId` | string | yes | The transactional message template to use. You can supply the numeric template ID or the trigger name. Example: `password-reset`. |
| `identifiers` | object | yes | Identifies the person represented by your transactional message by exactly one of id, email, or cio_id. |
| `identifiers.id` | string | no | Use the customer's ID identifier when your workspace identifies people by ID. Example: `user_123`. |
| `identifiers.email` | string | no | Use the customer's email identifier when your workspace identifies people by email. Example: `user@example.com`. |
| `identifiers.cioId` | string | no | Use the immutable Customer.io person identifier. Example: `3000001`. |
| `to` | string | yes | The message recipient or recipients. Example: `user@example.com`. |
| `from` | string | no | The verified sender address that the email is from. Example: `alerts@example.com`. |
| `subject` | string | no | Overrides the transactional template subject line. Example: `Reset your password`. |
| `body` | string | no | Overrides the transactional template HTML body. Example: `<p>Your reset link is here.</p>`. |
| `bodyPlain` | string | no | Overrides the plaintext body. Example: `Your reset link is here.`. |
| `messageData` | object | no | Key-value pairs referenced by liquid in your message. |
| `language` | string | no | Overrides language preferences for the recipient. Example: `en`. |
| `sendToUnsubscribed` | boolean | no | If false, the message is not sent to unsubscribed recipients. |
| `disableMessageRetention` | boolean | no | If true, the message body is not retained in delivery history. |
| `queueDraft` | boolean | no | If true, the message is queued as a draft instead of sent immediately. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sendAt` | number | no | Unix timestamp determining when the message will be sent. Example: `1772823600`. |
| `bodyAmp` | string | no | AMP-enabled email body. Example: `<p>AMP content</p>`. |
| `bcc` | string | no | Blind copy recipients. Example: `ops@example.com`. |
| `fakeBcc` | boolean | no | If true, Customer.io sends per-recipient copies instead of true BCC copies. |
| `replyTo` | string | no | The address that recipients can reply to. Example: `support@example.com`. |
| `preheader` | string | no | Preview text shown next to or under the subject line. Example: `Reset your password`. |
| `attachments` | object | no | A dictionary of attachments keyed by filename with base64-encoded contents. |
| `headers` | string | no | A JSON string containing an array of header objects. Example: `[object Object]`. |
| `disableCssPreprocessing` | boolean | no | If true, disables CSS preprocessing for the email. |
| `tracked` | boolean | no | If true, Customer.io tracks opens and link clicks in your message. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deliveryId": "string",
      "queuedAt": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deliveryId` | string | A unique identifier for the queued delivery. |
| `queuedAt` | number | Unix timestamp when Customer.io queued the message. |

## Native endpoint

Through the native Customer.io API, this operation is `POST /v1/send/email` (base URL `https://api.customer.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-transactional-email.md) for the provider-specific parameters and requirements.

