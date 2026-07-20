# Chaindesk: Create Mail Inbox

Creates a mail inbox in Chaindesk.

```
POST https://connect.mindcloud.co/v1/universal/chaindesk/latest/actions/create-mail-inbox
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chaindesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chaindesk/latest/actions/create-mail-inbox" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chaindesk/latest/actions/create-mail-inbox', {
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | no |  |
| `alias` | string | no |  |

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

Through the native Chaindesk API, this operation is `POST /mail-inboxes` (base URL `https://app.chaindesk.ai/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-mail-inbox.md) for the provider-specific parameters and requirements.

