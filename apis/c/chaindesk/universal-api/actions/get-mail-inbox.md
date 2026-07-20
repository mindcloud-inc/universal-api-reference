# Chaindesk: Get Mail Inbox

Retrieves a mail inbox from Chaindesk.

```
GET https://connect.mindcloud.co/v1/universal/chaindesk/latest/actions/get-mail-inbox
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chaindesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chaindesk/latest/actions/get-mail-inbox?connectionId=$CONNECTION_ID&mailInboxId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "mailInboxId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chaindesk/latest/actions/get-mail-inbox?${params}`, {
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
| `mailInboxId` | string | yes |  |

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

Through the native Chaindesk API, this operation is `GET /mail-inboxes/:mailInboxId` (base URL `https://app.chaindesk.ai/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-mail-inbox.md) for the provider-specific parameters and requirements.

