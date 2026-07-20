# Firebolt: Run Async SQL Query

Creates an asynchronous SQL query in Firebolt.

```
POST https://connect.mindcloud.co/v1/universal/firebolt/latest/actions/run-async-sql-query
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Firebolt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/firebolt/latest/actions/run-async-sql-query" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "engineUrl": "01abcde12345.api.us-east-1.app.firebolt.io",
  "sqlQuery": "START ENGINE my_engine"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/firebolt/latest/actions/run-async-sql-query', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "engineUrl": "01abcde12345.api.us-east-1.app.firebolt.io",
    "sqlQuery": "START ENGINE my_engine"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `engineUrl` | string | yes | Firebolt engine URL host or engine endpoint returned by Firebolt. Example: `01abcde12345.api.us-east-1.app.firebolt.io`. |
| `sqlQuery` | string | yes | Async SQL statement to submit. Example: `START ENGINE my_engine`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `database` | string | no | Database to target for user-engine async queries. Example: `analytics`. |
| `engineName` | string | no | User engine name to target when submitting an async query to a user engine. Example: `mc_fb_act_20260422_engine`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "monitorSql": "string",
      "token": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `monitorSql` | string |  |
| `token` | string |  |

## Native endpoint

Through the native Firebolt API, this operation is `POST https://:engineUrl` (base URL `https://api.app.firebolt.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/run-async-sql-query.md) for the provider-specific parameters and requirements.

