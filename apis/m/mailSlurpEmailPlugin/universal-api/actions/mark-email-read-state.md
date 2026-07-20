# MailSlurp Email Plugin: Mark Email Read State

Updates an email's read state in MailSlurp.

```
PUT https://connect.mindcloud.co/v1/universal/mailSlurpEmailPlugin/latest/actions/mark-email-read-state
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailSlurp Email Plugin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mailSlurpEmailPlugin/latest/actions/mark-email-read-state" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailSlurpEmailPlugin/latest/actions/mark-email-read-state', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `emailId` | string | no | The MailSlurp email ID to update. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "from": "string",
      "id": "string",
      "inboxId": "string",
      "read": true,
      "subject": "string",
      "to": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `from` | string |  |
| `id` | string |  |
| `inboxId` | string |  |
| `read` | boolean |  |
| `subject` | string |  |
| `to` | array<string> |  |

## Native endpoint

Through the native MailSlurp Email Plugin API, this operation is `PATCH /emails/:emailId/read` (base URL `https://api.mailslurp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/mark-email-read-state.md) for the provider-specific parameters and requirements.

