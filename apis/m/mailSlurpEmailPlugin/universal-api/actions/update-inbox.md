# MailSlurp Email Plugin: Update Inbox

Updates an existing inbox in MailSlurp.

```
PUT https://connect.mindcloud.co/v1/universal/mailSlurpEmailPlugin/latest/actions/update-inbox
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailSlurp Email Plugin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mailSlurpEmailPlugin/latest/actions/update-inbox" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailSlurpEmailPlugin/latest/actions/update-inbox', {
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
| `inboxId` | string | no | The MailSlurp inbox ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "description": "string",
      "emailAddress": "ava@example.com",
      "expiresAt": "string",
      "favourite": true,
      "id": "string",
      "inboxType": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `description` | string |  |
| `emailAddress` | string |  |
| `expiresAt` | string |  |
| `favourite` | boolean |  |
| `id` | string |  |
| `inboxType` | string |  |
| `name` | string |  |

## Native endpoint

Through the native MailSlurp Email Plugin API, this operation is `PATCH /inboxes/:inboxId` (base URL `https://api.mailslurp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-inbox.md) for the provider-specific parameters and requirements.

