# EmailOctopus: List Contacts

Retrieves contacts from an EmailOctopus list.

```
GET https://connect.mindcloud.co/v1/universal/emailOctopus/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EmailOctopus `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/emailOctopus/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0&listId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "listId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/emailOctopus/latest/actions/list-contacts?${params}`, {
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

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native EmailOctopus API returns.

## Native endpoint

Through the native EmailOctopus API, this operation is `GET /lists/:listId/contacts` (base URL `https://emailoctopus.com/api/1.6`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

