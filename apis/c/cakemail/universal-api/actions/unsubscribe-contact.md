# Cakemail: Unsubscribe Contact

Unsubscribes a contact from a Cakemail list.

```
PUT https://connect.mindcloud.co/v1/universal/cakemail/latest/actions/unsubscribe-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cakemail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/cakemail/latest/actions/unsubscribe-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "listId": 1,
  "contactId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cakemail/latest/actions/unsubscribe-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "listId": 1,
    "contactId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `listId` | number | yes | Cakemail list ID. |
| `contactId` | number | yes | Cakemail contact ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Cakemail API returns.

## Native endpoint

Through the native Cakemail API, this operation is `POST /lists/:listId/contacts/:contactId/unsubscribe` (base URL `https://api.cakemail.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/unsubscribe-contact.md) for the provider-specific parameters and requirements.

