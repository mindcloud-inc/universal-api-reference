# Basecamp: Get Todo

Retrieves a to-do from Basecamp.

```
GET https://connect.mindcloud.co/v1/universal/basecamp/latest/actions/get-todo
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Basecamp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/basecamp/latest/actions/get-todo?connectionId=$CONNECTION_ID&accountId=6172410&todoId=9660797208" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "6172410",
  "todoId": "9660797208"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/basecamp/latest/actions/get-todo?${params}`, {
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
| `todoId` | number | yes | To-do ID returned by List Todos or Create Todo. Example: `9660797208`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Basecamp API returns.

## Native endpoint

Through the native Basecamp API, this operation is `GET /:accountId/todos/:todoId.json` (base URL `https://3.basecampapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-todo.md) for the provider-specific parameters and requirements.

