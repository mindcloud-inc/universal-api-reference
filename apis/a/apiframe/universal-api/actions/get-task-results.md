# Apiframe: Get Task Results

Retrieves multiple Apiframe task results by task IDs.

```
GET https://connect.mindcloud.co/v1/universal/apiframe/latest/actions/get-task-results
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Apiframe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/apiframe/latest/actions/get-task-results?connectionId=$CONNECTION_ID&task_ids%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "task_ids[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/apiframe/latest/actions/get-task-results?${params}`, {
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
| `task_ids[]` | array<string> | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Apiframe API returns.

## Native endpoint

Through the native Apiframe API, this operation is `POST /fetch-many` (base URL `https://api.apiframe.pro`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-task-results.md) for the provider-specific parameters and requirements.

