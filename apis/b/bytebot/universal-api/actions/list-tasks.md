# bytebot: List Tasks

Retrieves a list of tasks from bytebot.

```
GET https://connect.mindcloud.co/v1/universal/bytebot/latest/actions/list-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a bytebot `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bytebot/latest/actions/list-tasks?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bytebot/latest/actions/list-tasks?${params}`, {
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
| `status` | string | no | Optional task status filter. Supported live values include PENDING, IN_PROGRESS, NEEDS_HELP, NEEDS_REVIEW, COMPLETED, CANCELLED, and FAILED. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native bytebot API returns.

## Native endpoint

Through the native bytebot API, this operation is `GET {{credentials.agentBaseUrl}}/tasks` (base URL `{{credentials.agentBaseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-tasks.md) for the provider-specific parameters and requirements.

