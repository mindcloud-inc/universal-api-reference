# Firebolt: Merge Rows

Creates row merges in Firebolt.

```
POST https://connect.mindcloud.co/v1/universal/firebolt/latest/actions/merge-rows
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Firebolt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/firebolt/latest/actions/merge-rows" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "engineHost": "account-1-mindcloud.api.us-east-1.app.firebolt.io",
  "targetTableName": "mc_fb_act_20260422_table",
  "sourceClause": "(SELECT 4 AS id, '\''fresh'\'' AS status, CURRENT_TIMESTAMP AS updated_at, '\''merged-four'\'' AS value) AS src",
  "joinCondition": "mc_fb_act_20260422_table.id = src.id",
  "whenClauses": "WHEN MATCHED THEN UPDATE SET status = src.status, updated_at = src.updated_at, value = src.value WHEN NOT MATCHED THEN INSERT (id, status, updated_at, value) VALUES (src.id, src.status, src.updated_at, src.value)"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/firebolt/latest/actions/merge-rows', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "engineHost": "account-1-mindcloud.api.us-east-1.app.firebolt.io",
    "targetTableName": "mc_fb_act_20260422_table",
    "sourceClause": "(SELECT 4 AS id, 'fresh' AS status, CURRENT_TIMESTAMP AS updated_at, 'merged-four' AS value) AS src",
    "joinCondition": "mc_fb_act_20260422_table.id = src.id",
    "whenClauses": "WHEN MATCHED THEN UPDATE SET status = src.status, updated_at = src.updated_at, value = src.value WHEN NOT MATCHED THEN INSERT (id, status, updated_at, value) VALUES (src.id, src.status, src.updated_at, src.value)"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `engineHost` | string | yes | Firebolt user-engine host, for example account-1-mindcloud.api.us-east-1.app.firebolt.io. Example: `account-1-mindcloud.api.us-east-1.app.firebolt.io`. |
| `targetTableName` | string | yes | Target table to merge into. Example: `mc_fb_act_20260422_table`. |
| `sourceClause` | string | yes | USING clause source, such as a SELECT subquery with an alias. Example: `(SELECT 4 AS id, 'fresh' AS status, CURRENT_TIMESTAMP AS updated_at, 'merged-four' AS value) AS src`. |
| `joinCondition` | string | yes | ON clause that matches source rows to target rows. Example: `mc_fb_act_20260422_table.id = src.id`. |
| `whenClauses` | string | yes | One or more WHEN clauses that define the merge behavior. Example: `WHEN MATCHED THEN UPDATE SET status = src.status, updated_at = src.updated_at, value = src.value WHEN NOT MATCHED THEN INSERT (id, status, updated_at, value) VALUES (src.id, src.status, src.updated_at, src.value)`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `engineName` | string | no | Optional user engine name when routing through a shared user-engine host. Example: `mc_fb_act_20260422_engine`. |
| `database` | string | no | Optional database to target for the merge statement. Example: `mc_fb_act_20260422_db`. |

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

Through the native Firebolt API, this operation is `POST https://:engineHost` (base URL `https://api.app.firebolt.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/merge-rows.md) for the provider-specific parameters and requirements.

