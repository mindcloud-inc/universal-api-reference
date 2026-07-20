# MailSlurp Email Plugin: Get Inbox

Retrieves an inbox and its details from MailSlurp.

```
GET https://connect.mindcloud.co/v1/universal/mailSlurpEmailPlugin/latest/actions/get-inbox
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailSlurp Email Plugin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailSlurpEmailPlugin/latest/actions/get-inbox?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailSlurpEmailPlugin/latest/actions/get-inbox?${params}`, {
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

Through the native MailSlurp Email Plugin API, this operation is `GET /inboxes/:inboxId` (base URL `https://api.mailslurp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-inbox.md) for the provider-specific parameters and requirements.

