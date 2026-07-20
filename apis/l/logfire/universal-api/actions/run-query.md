# Logfire: Run Query

Runs a query against Logfire data.

```
GET https://connect.mindcloud.co/v1/universal/logfire/latest/actions/run-query
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Logfire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/logfire/latest/actions/run-query?connectionId=$CONNECTION_ID&sql=SELECT%20start_timestamp%2C%20message%20FROM%20records%20LIMIT%2010" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sql": "SELECT start_timestamp, message FROM records LIMIT 10"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/logfire/latest/actions/run-query?${params}`, {
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
| `sql` | string | yes | SQL query to execute against the Logfire project. Example: `SELECT start_timestamp, message FROM records LIMIT 10`. |
| `limit` | number | no | Maximum number of rows to return. Logfire defaults to 500 and allows up to 10,000. Example: `100`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `minTimestamp` | date | no | Lower timestamp bound for records or metrics returned by the query. Example: `2026-04-01T00:00:00Z`. |
| `maxTimestamp` | date | no | Upper timestamp bound for records or metrics returned by the query. Example: `2026-04-14T23:59:59Z`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Logfire API returns.

## Native endpoint

Through the native Logfire API, this operation is `GET /v1/query` (base URL `https://logfire-api.pydantic.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/run-query.md) for the provider-specific parameters and requirements.

