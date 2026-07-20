# Firebolt: Update Database

Updates an existing database in Firebolt.

```
PUT https://connect.mindcloud.co/v1/universal/firebolt/latest/actions/update-database
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Firebolt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/firebolt/latest/actions/update-database" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "engineHost": "01kjtg5w4vwy72rfew4r8vg135.api.us-east-1.app.firebolt.io",
  "databaseName": "mc_fb_act_20260422_db",
  "alterClause": "SET DESCRIPTION = '\''Updated by MindCloud test'\''"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/firebolt/latest/actions/update-database', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "engineHost": "01kjtg5w4vwy72rfew4r8vg135.api.us-east-1.app.firebolt.io",
    "databaseName": "mc_fb_act_20260422_db",
    "alterClause": "SET DESCRIPTION = 'Updated by MindCloud test'"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `engineHost` | string | yes | System engine host to execute the ALTER DATABASE statement against. Example: `01kjtg5w4vwy72rfew4r8vg135.api.us-east-1.app.firebolt.io`. |
| `databaseName` | string | yes | The Firebolt database to alter. Example: `mc_fb_act_20260422_db`. |
| `alterClause` | string | yes | The ALTER DATABASE clause, for example SET DESCRIPTION = 'Updated description' or RENAME TO new_database_name. Example: `SET DESCRIPTION = 'Updated by MindCloud test'`. |

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

Through the native Firebolt API, this operation is `POST https://:engineHost` (base URL `https://api.app.firebolt.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-database.md) for the provider-specific parameters and requirements.

