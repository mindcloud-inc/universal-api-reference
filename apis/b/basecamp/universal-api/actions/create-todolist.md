# Basecamp: Create Todolist

Creates a new to-do list in a Basecamp to-do set.

```
POST https://connect.mindcloud.co/v1/universal/basecamp/latest/actions/create-todolist
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Basecamp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/basecamp/latest/actions/create-todolist" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": "6172410",
  "todosetId": "9660796830",
  "name": "MindCloud Stage 3 Test List"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/basecamp/latest/actions/create-todolist', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": "6172410",
    "todosetId": "9660796830",
    "name": "MindCloud Stage 3 Test List"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | string | yes | Basecamp account ID (numeric string). Example: `6172410`. |
| `todosetId` | number | yes | To-do set ID from the project's dock.todoset entry. Example: `9660796830`. |
| `name` | string | yes | Name of the to-do list. Example: `MindCloud Stage 3 Test List`. |
| `description` | string | no | Optional Basecamp rich-text HTML description. Example: `<div>Optional details</div>`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Basecamp API returns.

## Native endpoint

Through the native Basecamp API, this operation is `POST /:accountId/todosets/:todosetId/todolists.json` (base URL `https://3.basecampapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-todolist.md) for the provider-specific parameters and requirements.

