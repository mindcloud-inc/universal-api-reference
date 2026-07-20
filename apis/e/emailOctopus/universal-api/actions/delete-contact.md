# EmailOctopus: Delete Contact

Deletes a contact from an EmailOctopus list.

```
DELETE https://connect.mindcloud.co/v1/universal/emailOctopus/latest/actions/delete-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EmailOctopus `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/emailOctopus/latest/actions/delete-contact?connectionId=$CONNECTION_ID&listId=string&memberId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "listId": "string",
  "memberId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/emailOctopus/latest/actions/delete-contact?${params}`, {
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
| `listId` | string | yes | The unique ID of the list. |
| `memberId` | string | yes | The unique ID of the contact. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native EmailOctopus API returns.

## Native endpoint

Through the native EmailOctopus API, this operation is `DELETE /lists/:listId/contacts/:memberId` (base URL `https://emailoctopus.com/api/1.6`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-contact.md) for the provider-specific parameters and requirements.

