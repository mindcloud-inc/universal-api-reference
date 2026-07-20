# Basecamp: Create Todo

Creates a new to-do in a Basecamp to-do list.

```
POST https://connect.mindcloud.co/v1/universal/basecamp/latest/actions/create-todo
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Basecamp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/basecamp/latest/actions/create-todo" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": "6172410",
  "todolistId": "9661708392",
  "content": "MindCloud Stage 3 Test Todo"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/basecamp/latest/actions/create-todo', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": "6172410",
    "todolistId": "9661708392",
    "content": "MindCloud Stage 3 Test Todo"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | string | yes | Example: `6172410`. |
| `todolistId` | number | yes | Example: `9661708392`. |
| `content` | string | yes | Example: `MindCloud Stage 3 Test Todo`. |
| `description` | string | no | Example: `<div>MindCloud Batch C validation</div>`. |
| `assigneeIds` | list<number> | no | Accepts multiple values as an array. |
| `dueOn` | date | no | Example: `2026-03-17`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `startsOn` | date | no | Example: `2026-03-15`. |
| `completionSubscriberIds` | list<number> | no | Accepts multiple values as an array. |
| `notify` | boolean | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Basecamp API returns.

## Native endpoint

Through the native Basecamp API, this operation is `POST /:accountId/todolists/:todolistId/todos.json` (base URL `https://3.basecampapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-todo.md) for the provider-specific parameters and requirements.

