# Firebolt: Delete Rows

Deletes existing rows from Firebolt.

```
DELETE https://connect.mindcloud.co/v1/universal/firebolt/latest/actions/delete-rows
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Firebolt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/firebolt/latest/actions/delete-rows?connectionId=$CONNECTION_ID&engineHost=account-1-mindcloud.api.us-east-1.app.firebolt.io&tableName=mc_fb_act_20260422_table" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "engineHost": "account-1-mindcloud.api.us-east-1.app.firebolt.io",
  "tableName": "mc_fb_act_20260422_table"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/firebolt/latest/actions/delete-rows?${params}`, {
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
| `engineHost` | string | yes | User engine host to execute the DELETE statement against. Example: `account-1-mindcloud.api.us-east-1.app.firebolt.io`. |
| `tableName` | string | yes | The Firebolt table to delete rows from. Example: `mc_fb_act_20260422_table`. |
| `whereClause` | string | no | Optional WHERE clause to restrict which rows are deleted. Example: `id = 4`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `engineName` | string | no | Optional engine name to send as the Firebolt engine query parameter. Example: `mc_fb_act_20260422_engine`. |
| `database` | string | no | Optional Firebolt database to execute the DELETE statement in. Example: `mc_fb_act_20260422_db`. |
| `tableAlias` | string | no | Optional alias for the target table. Example: `t`. |
| `usingClause` | string | no | Optional USING clause contents to join other tables into the DELETE statement. Example: `other_table ot`. |
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

Through the native Firebolt API, this operation is `POST https://:engineHost` (base URL `https://api.app.firebolt.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-rows.md) for the provider-specific parameters and requirements.

