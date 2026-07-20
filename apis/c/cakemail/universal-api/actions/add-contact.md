# Cakemail: Add Contact

Creates a new contact in a Cakemail list.

```
POST https://connect.mindcloud.co/v1/universal/cakemail/latest/actions/add-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cakemail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cakemail/latest/actions/add-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "listId": 1,
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cakemail/latest/actions/add-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "listId": 1,
    "email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `listId` | number | yes | Cakemail list ID. |
| `email` | string | yes | Email address for the contact. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sendDoubleOptIn` | string | no | Whether and when Cakemail should send a double opt-in confirmation email. Default: `false`. |
| `resubscribe` | boolean | no | Whether to resubscribe the contact when applicable. Default: `true`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Cakemail API returns.

## Native endpoint

Through the native Cakemail API, this operation is `POST /lists/:listId/contacts` (base URL `https://api.cakemail.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-contact.md) for the provider-specific parameters and requirements.

