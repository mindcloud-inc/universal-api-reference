# MailSlurp Email Plugin: Create Inbox With Options

Creates a new inbox in MailSlurp with custom options.

```
POST https://connect.mindcloud.co/v1/universal/mailSlurpEmailPlugin/latest/actions/create-inbox-with-options
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailSlurp Email Plugin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mailSlurpEmailPlugin/latest/actions/create-inbox-with-options" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailSlurpEmailPlugin/latest/actions/create-inbox-with-options', {
  method: 'POST',
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

Through the native MailSlurp Email Plugin API, this operation is `POST /inboxes/withOptions` (base URL `https://api.mailslurp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-inbox-with-options.md) for the provider-specific parameters and requirements.

