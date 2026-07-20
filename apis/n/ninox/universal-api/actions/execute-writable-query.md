# Ninox: Execute Writable Query

Executes a writable database query in Ninox.

```
PUT https://connect.mindcloud.co/v1/universal/ninox/latest/actions/execute-writable-query
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ninox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/ninox/latest/actions/execute-writable-query" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "teamId": "team_id",
  "dbId": "database_id",
  "query": "(select Contact).'\''First Name'\''"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ninox/latest/actions/execute-writable-query', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "teamId": "team_id",
    "dbId": "database_id",
    "query": "(select Contact).'First Name'"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `teamId` | string | yes | The team ID that owns the target database. Example: `team_id`. |
| `dbId` | string | yes | The Ninox database ID. Example: `database_id`. |
| `query` | string | yes | The writable Ninox query to execute. Example: `(select Contact).'First Name'`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Ninox API returns.

## Native endpoint

Through the native Ninox API, this operation is `POST teams/:teamId/databases/:dbId/exec` (base URL `https://api.ninox.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/execute-writable-query.md) for the provider-specific parameters and requirements.

