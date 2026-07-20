# Wooxy: Delete Contact

Deletes an existing contact from Wooxy.

```
DELETE https://connect.mindcloud.co/v1/universal/wooxy/latest/actions/delete-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wooxy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/wooxy/latest/actions/delete-contact?connectionId=$CONNECTION_ID&contactListId=yourContactListId" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contactListId": "yourContactListId"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wooxy/latest/actions/delete-contact?${params}`, {
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
| `contactListId` | string | yes | Wooxy contact list ID. Example: `yourContactListId`. |
| `emails[]` | array<string> | no | Array of emails to remove. Example: `user@example.com`. |
| `phoneNumbers[]` | array<string> | no | Array of phone numbers to remove. Example: `+15555555555`. |
| `userIds[]` | array<string> | no | Array of user IDs to remove. Example: `stageThreeUser`. |
| `webHookUri` | string | no | Optional callback URL for async status notifications. Example: `https://example.com/contact-status`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Wooxy API returns.

## Native endpoint

Through the native Wooxy API, this operation is `POST v3/contacts/remove` (base URL `https://api.wooxy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-contact.md) for the provider-specific parameters and requirements.

