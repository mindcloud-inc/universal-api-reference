# Wooxy: Create Contact

Creates a new contact in Wooxy.

```
POST https://connect.mindcloud.co/v1/universal/wooxy/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wooxy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/wooxy/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactListId": "yourContactListId",
  "contacts[]": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wooxy/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactListId": "yourContactListId",
    "contacts[]": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactListId` | string | yes | Wooxy contact list ID. Example: `yourContactListId`. |
| `contacts[]` | array<object> | yes | Array of contact objects to create. Example: `[object Object]`. |
| `webHookUri` | string | no | Optional callback URL for async status notifications. Example: `https://example.com/contact-status`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Wooxy API returns.

## Native endpoint

Through the native Wooxy API, this operation is `POST v3/contacts/add` (base URL `https://api.wooxy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

