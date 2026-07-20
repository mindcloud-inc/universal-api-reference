# Firebolt: Run Sync SQL Query

Retrieves synchronous query results from Firebolt.

```
GET https://connect.mindcloud.co/v1/universal/firebolt/latest/actions/run-sync-sql-query
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Firebolt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/firebolt/latest/actions/run-sync-sql-query?connectionId=$CONNECTION_ID&engineUrl=01abcde12345.api.us-east-1.app.firebolt.io&sqlQuery=SELECT%2042%20AS%20answer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "engineUrl": "01abcde12345.api.us-east-1.app.firebolt.io",
  "sqlQuery": "SELECT 42 AS answer"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/firebolt/latest/actions/run-sync-sql-query?${params}`, {
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
| `engineUrl` | string | yes | The Firebolt engine host to send the SQL request to. Example: `01abcde12345.api.us-east-1.app.firebolt.io`. |
| `sqlQuery` | string | yes | A single Firebolt SQL statement to execute synchronously. Example: `SELECT 42 AS answer`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `database` | string | no | Optional database name. Required for user-engine queries and omitted for system-engine queries. Example: `analytics`. |
| `engineName` | string | no | User engine name to target when querying a user engine. Example: `mc_fb_act_20260422_engine`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Firebolt API returns.

## Native endpoint

Through the native Firebolt API, this operation is `POST https://:engineUrl` (base URL `https://api.app.firebolt.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/run-sync-sql-query.md) for the provider-specific parameters and requirements.

