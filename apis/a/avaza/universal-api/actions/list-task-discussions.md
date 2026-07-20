# Avaza: List Task Discussions

Retrieves task discussion messages from Avaza.

```
GET https://connect.mindcloud.co/v1/universal/avaza/latest/actions/list-task-discussions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Avaza `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/avaza/latest/actions/list-task-discussions?connectionId=$CONNECTION_ID&taskid=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskid": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/avaza/latest/actions/list-task-discussions?${params}`, {
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
| `taskid` | number | yes | The TaskID of the Task to retrieve messages for |
| `startitem` | number | no | the ReponseID of the comment from which the page of results should start. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Avaza API returns.

## Native endpoint

Through the native Avaza API, this operation is `GET /api/TaskDiscussion` (base URL `https://api.avaza.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-task-discussions.md) for the provider-specific parameters and requirements.

