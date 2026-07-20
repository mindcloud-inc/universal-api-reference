# Chaindesk: Update Mail Inbox

Updates a mail inbox in Chaindesk.

```
PUT https://connect.mindcloud.co/v1/universal/chaindesk/latest/actions/update-mail-inbox
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chaindesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/chaindesk/latest/actions/update-mail-inbox" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "mailInboxId": "string",
  "name": "Ava Chen",
  "alias": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chaindesk/latest/actions/update-mail-inbox', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "mailInboxId": "string",
    "name": "Ava Chen",
    "alias": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `mailInboxId` | string | yes |  |
| `name` | string | yes |  |
| `alias` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alias": "string",
      "createdAt": "string",
      "customEmail": "ava@example.com",
      "customEmailVerificationTokenId": "ava@example.com",
      "description": "string",
      "fromName": "Ava Chen",
      "id": "string",
      "isCustomEmailVerified": true,
      "name": "Ava Chen",
      "organizationId": "string",
      "showBranding": true,
      "signature": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alias` | string |  |
| `createdAt` | string |  |
| `customEmail` | string |  |
| `customEmailVerificationTokenId` | string |  |
| `description` | string |  |
| `fromName` | string |  |
| `id` | string |  |
| `isCustomEmailVerified` | boolean |  |
| `name` | string |  |
| `organizationId` | string |  |
| `showBranding` | boolean |  |
| `signature` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Chaindesk API, this operation is `PATCH /mail-inboxes/:mailInboxId` (base URL `https://app.chaindesk.ai/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-mail-inbox.md) for the provider-specific parameters and requirements.

