# Ninox: Execute Read-Only Query Via POST

Executes a read-only database query in Ninox.

```
GET https://connect.mindcloud.co/v1/universal/ninox/latest/actions/execute-read-only-query-via-post
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ninox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ninox/latest/actions/execute-read-only-query-via-post?connectionId=$CONNECTION_ID&teamId=team_id&dbId=database_id&query=(select%20Contact).'First%20Name'" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "teamId": "team_id",
  "dbId": "database_id",
  "query": "(select Contact).'First Name'"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ninox/latest/actions/execute-read-only-query-via-post?${params}`, {
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
| `teamId` | string | yes | The team ID that owns the target database. Example: `team_id`. |
| `dbId` | string | yes | The Ninox database ID. Example: `database_id`. |
| `query` | string | yes | The read-only Ninox query to execute. Example: `(select Contact).'First Name'`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Ninox API returns.

## Native endpoint

Through the native Ninox API, this operation is `POST teams/:teamId/databases/:dbId/query` (base URL `https://api.ninox.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/execute-read-only-query-via-post.md) for the provider-specific parameters and requirements.

