# Cakemail: Delete Contact

Deletes a contact from a Cakemail list.

```
DELETE https://connect.mindcloud.co/v1/universal/cakemail/latest/actions/delete-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cakemail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/cakemail/latest/actions/delete-contact?connectionId=$CONNECTION_ID&listId=1&contactId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "listId": "1",
  "contactId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cakemail/latest/actions/delete-contact?${params}`, {
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
| `listId` | number | yes | Cakemail list ID. |
| `contactId` | number | yes | Cakemail contact ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Cakemail API returns.

## Native endpoint

Through the native Cakemail API, this operation is `DELETE /lists/:listId/contacts/:contactId` (base URL `https://api.cakemail.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-contact.md) for the provider-specific parameters and requirements.

