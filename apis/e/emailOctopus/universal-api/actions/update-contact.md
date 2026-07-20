# EmailOctopus: Update Contact

Updates a contact in an EmailOctopus list.

```
PUT https://connect.mindcloud.co/v1/universal/emailOctopus/latest/actions/update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EmailOctopus `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/emailOctopus/latest/actions/update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "listId": "string",
  "memberId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/emailOctopus/latest/actions/update-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "listId": "string",
    "memberId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email_address` | string | no | The updated contact email address. |
| `fields` | object | no | Custom field values for the contact. |
| `listId` | string | yes | The unique ID of the list. |
| `memberId` | string | yes | The unique ID of the contact. |
| `status` | string | no | The subscription status for the contact. |
| `tags[]` | array<string> | no | Tags to apply to the contact. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native EmailOctopus API returns.

## Native endpoint

Through the native EmailOctopus API, this operation is `PUT /lists/:listId/contacts/:memberId` (base URL `https://emailoctopus.com/api/1.6`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact.md) for the provider-specific parameters and requirements.

