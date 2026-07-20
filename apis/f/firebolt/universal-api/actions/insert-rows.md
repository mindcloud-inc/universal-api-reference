# Firebolt: Insert Rows

Creates row inserts in Firebolt.

```
POST https://connect.mindcloud.co/v1/universal/firebolt/latest/actions/insert-rows
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Firebolt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/firebolt/latest/actions/insert-rows" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "engineHost": "account-1-mindcloud.api.us-east-1.app.firebolt.io",
  "tableName": "mc_fb_act_20260422_table",
  "sourceClause": "VALUES (3, '\''pending'\'', CURRENT_TIMESTAMP, '\''inserted-three'\'')"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/firebolt/latest/actions/insert-rows', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "engineHost": "account-1-mindcloud.api.us-east-1.app.firebolt.io",
    "tableName": "mc_fb_act_20260422_table",
    "sourceClause": "VALUES (3, 'pending', CURRENT_TIMESTAMP, 'inserted-three')"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `engineHost` | string | yes | Firebolt user-engine host, for example account-1-mindcloud.api.us-east-1.app.firebolt.io. Example: `account-1-mindcloud.api.us-east-1.app.firebolt.io`. |
| `tableName` | string | yes | Target table to insert rows into. Example: `mc_fb_act_20260422_table`. |
| `sourceClause` | string | yes | VALUES tuples or a SELECT query to insert. Example: `VALUES (3, 'pending', CURRENT_TIMESTAMP, 'inserted-three')`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `engineName` | string | no | Optional user engine name when routing through a shared user-engine host. Example: `mc_fb_act_20260422_engine`. |
| `database` | string | no | Optional database to target for the insert statement. Example: `mc_fb_act_20260422_db`. |
| `columnList` | string | no | Optional comma-separated target columns for the insert statement. Example: `id, status, updated_at, value`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "meta": [
        {}
      ],
      "query": {},
      "rows": 1,
      "statistics": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | Returned data rows. |
| `meta` | array<object> | Column metadata for the response. |
| `query` | object | Firebolt query metadata. |
| `rows` | number | Number of rows returned in the data payload. |
| `statistics` | object | Firebolt execution statistics. |

## Native endpoint

Through the native Firebolt API, this operation is `POST https://:engineHost` (base URL `https://api.app.firebolt.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/insert-rows.md) for the provider-specific parameters and requirements.

