# Basecamp: Complete Todo

Marks a to-do as completed in Basecamp.

```
PUT https://connect.mindcloud.co/v1/universal/basecamp/latest/actions/complete-todo
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Basecamp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/basecamp/latest/actions/complete-todo" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": "6172410",
  "todoId": "9660797208"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/basecamp/latest/actions/complete-todo', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": "6172410",
    "todoId": "9660797208"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | string | yes | Example: `6172410`. |
| `todoId` | number | yes | Example: `9660797208`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Basecamp API returns.

## Native endpoint

Through the native Basecamp API, this operation is `POST /:accountId/todos/:todoId/completion.json` (base URL `https://3.basecampapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/complete-todo.md) for the provider-specific parameters and requirements.

