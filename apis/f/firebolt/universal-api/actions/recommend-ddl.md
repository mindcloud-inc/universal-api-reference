# Firebolt: Recommend DDL

Retrieves DDL recommendations from Firebolt.

```
GET https://connect.mindcloud.co/v1/universal/firebolt/latest/actions/recommend-ddl
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Firebolt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/firebolt/latest/actions/recommend-ddl?connectionId=$CONNECTION_ID&engineUrl=account-1-mindcloud.api.us-east-1.app.firebolt.io&engineName=mc_fb_act_20260422_engine&database=mc_fb_act_20260422_db&tableName=mc_stage3_20260422_table1&workloadQuery=SELECT%20'SELECT%20*%20FROM%20mc_stage3_20260422_table1%20WHERE%20id%20%3D%201'" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "engineUrl": "account-1-mindcloud.api.us-east-1.app.firebolt.io",
  "engineName": "mc_fb_act_20260422_engine",
  "database": "mc_fb_act_20260422_db",
  "tableName": "mc_stage3_20260422_table1",
  "workloadQuery": "SELECT 'SELECT * FROM mc_stage3_20260422_table1 WHERE id = 1'"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/firebolt/latest/actions/recommend-ddl?${params}`, {
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
| `engineUrl` | string | yes | Firebolt user engine host, for example account-1-mindcloud.api.us-east-1.app.firebolt.io. Example: `account-1-mindcloud.api.us-east-1.app.firebolt.io`. |
| `engineName` | string | yes | Name of the user engine, for example mc_fb_act_20260422_engine. Example: `mc_fb_act_20260422_engine`. |
| `database` | string | yes | Database to use for the statement. Example: `mc_fb_act_20260422_db`. |
| `tableName` | string | yes | Table name to optimize. Example: `mc_stage3_20260422_table1`. |
| `workloadQuery` | string | yes | SELECT statement that returns exactly one TEXT column containing workload SQL. Example: `SELECT 'SELECT * FROM mc_stage3_20260422_table1 WHERE id = 1'`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Firebolt API returns.

## Native endpoint

Through the native Firebolt API, this operation is `POST https://:engineUrl` (base URL `https://api.app.firebolt.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/recommend-ddl.md) for the provider-specific parameters and requirements.

