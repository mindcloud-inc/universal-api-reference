# Firebolt: Update Rows

Updates existing rows in Firebolt.

```
PUT https://connect.mindcloud.co/v1/universal/firebolt/latest/actions/update-rows
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Firebolt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/firebolt/latest/actions/update-rows" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "engineHost": "account-1-mindcloud.api.us-east-1.app.firebolt.io",
  "tableName": "mc_fb_act_20260422_table",
  "setClause": "status = '\''updated'\'', updated_at = CURRENT_TIMESTAMP, value = '\''updated-three'\''"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/firebolt/latest/actions/update-rows', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "engineHost": "account-1-mindcloud.api.us-east-1.app.firebolt.io",
    "tableName": "mc_fb_act_20260422_table",
    "setClause": "status = 'updated', updated_at = CURRENT_TIMESTAMP, value = 'updated-three'"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `engineHost` | string | yes | User engine host to execute the UPDATE statement against. Example: `account-1-mindcloud.api.us-east-1.app.firebolt.io`. |
| `tableName` | string | yes | The Firebolt table to update. Example: `mc_fb_act_20260422_table`. |
| `setClause` | string | yes | The UPDATE SET clause, for example status = 'archived', updated_at = CURRENT_TIMESTAMP. Example: `status = 'updated', updated_at = CURRENT_TIMESTAMP, value = 'updated-three'`. |
| `whereClause` | string | no | Optional WHERE clause to restrict which rows are updated. Example: `id = 3`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `engineName` | string | no | Optional engine name to send as the Firebolt engine query parameter. Example: `mc_fb_act_20260422_engine`. |
| `database` | string | no | Optional Firebolt database to execute the UPDATE statement in. Example: `mc_fb_act_20260422_db`. |
| `tableAlias` | string | no | Optional alias for the target table. Example: `t`. |
| `fromClause` | string | no | Optional FROM clause contents to join other tables into the UPDATE statement. Example: `other_table ot`. |
| `settingsClause` | string | no | Optional WITH settings clause contents for query settings overrides. Example: `max_memory = 2147483648`. |

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

Through the native Firebolt API, this operation is `POST https://:engineHost` (base URL `https://api.app.firebolt.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-rows.md) for the provider-specific parameters and requirements.

