# EmailOctopus: Create Contact

Creates a contact in an EmailOctopus list.

```
POST https://connect.mindcloud.co/v1/universal/emailOctopus/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EmailOctopus `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/emailOctopus/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email_address": "ava@example.com",
  "listId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/emailOctopus/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email_address": "ava@example.com",
    "listId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email_address` | string | yes | The contact email address. |
| `fields` | object | no | Custom field values for the contact. |
| `listId` | string | yes | The unique ID of the list. |
| `status` | string | no | The subscription status for the contact. |
| `tags[]` | array<string> | no | Tags to apply to the contact. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native EmailOctopus API returns.

## Native endpoint

Through the native EmailOctopus API, this operation is `POST /lists/:listId/contacts` (base URL `https://emailoctopus.com/api/1.6`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

