# Basecamp: List Todolists

Retrieves to-do lists from a Basecamp to-do set.

```
GET https://connect.mindcloud.co/v1/universal/basecamp/latest/actions/list-todolists
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Basecamp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/basecamp/latest/actions/list-todolists?connectionId=$CONNECTION_ID&accountId=6172410&todosetId=9660796929" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "6172410",
  "todosetId": "9660796929"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/basecamp/latest/actions/list-todolists?${params}`, {
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
| `accountId` | string | yes | Basecamp account ID (numeric string). Example: `6172410`. |
| `todosetId` | number | yes | To-do set ID from the project's dock.todoset entry. Example: `9660796929`. |
| `status` | list<string> | no | Optional todolist status selector. One of: `active`, `archived`, `trashed`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Basecamp API returns.

## Native endpoint

Through the native Basecamp API, this operation is `GET /:accountId/todosets/:todosetId/todolists.json` (base URL `https://3.basecampapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-todolists.md) for the provider-specific parameters and requirements.

