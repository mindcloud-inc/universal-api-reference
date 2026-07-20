# lemlist: Send Email

Sends an email from lemlist inbox.

```
POST https://connect.mindcloud.co/v1/universal/lemlist/latest/actions/send-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a lemlist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/lemlist/latest/actions/send-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sendUserId": "usr_h47tiJr87Zn7XtQHi",
  "sendUserEmail": "john@example.com",
  "sendUserMailboxId": "usm_CE8QtNtgMjTHjfaL8",
  "contactId": "ctc_yHXD3NWjPg7Z9MuWZ",
  "leadId": "lea_7HAh3odqPKamkBTv9",
  "subject": "Follow up",
  "message": "<p>Hello,</p><p>Following up on our conversation...</p>"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lemlist/latest/actions/send-email', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sendUserId": "usr_h47tiJr87Zn7XtQHi",
    "sendUserEmail": "john@example.com",
    "sendUserMailboxId": "usm_CE8QtNtgMjTHjfaL8",
    "contactId": "ctc_yHXD3NWjPg7Z9MuWZ",
    "leadId": "lea_7HAh3odqPKamkBTv9",
    "subject": "Follow up",
    "message": "<p>Hello,</p><p>Following up on our conversation...</p>"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sendUserId` | string | yes | Sender user ID. Example: `usr_h47tiJr87Zn7XtQHi`. |
| `sendUserEmail` | string | yes | Sender email address. Example: `john@example.com`. |
| `sendUserMailboxId` | string | yes | Sender mailbox ID. Example: `usm_CE8QtNtgMjTHjfaL8`. |
| `contactId` | string | yes | Contact ID. Example: `ctc_yHXD3NWjPg7Z9MuWZ`. |
| `leadId` | string | yes | Lead ID. Example: `lea_7HAh3odqPKamkBTv9`. |
| `subject` | string | yes | Email subject. Example: `Follow up`. |
| `message` | string | yes | Email message (HTML). Example: `<p>Hello,</p><p>Following up on our conversation...</p>`. |
| `cc[]` | array<string> | no | CC email addresses. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ok": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ok` | boolean | Whether lemlist accepted the email send request. |

## Native endpoint

Through the native lemlist API, this operation is `POST /inbox/email` (base URL `https://api.lemlist.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-email.md) for the provider-specific parameters and requirements.

