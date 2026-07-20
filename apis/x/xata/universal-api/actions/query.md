# Xata: Execute SQL query



```
GET https://connect.mindcloud.co/v1/universal/xata/latest/actions/query
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Xata `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xata/latest/actions/query?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xata/latest/actions/query?${params}`, {
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
| `query` | string | no | SQL query to execute (single query mode). |
| `params[]` | array | no | Positional parameters for the query (`$1`, `$2`, ...). |
| `queries[]` | array | no | Array of queries for batch execution within a single transaction. |
| `arrayMode` | boolean | no | Override array mode for this query (single query mode only). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "command": "string",
      "fields": [
        {}
      ],
      "results": [
        {}
      ],
      "rowAsArray": true,
      "rowCount": 1,
      "rows": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `command` | string | PostgreSQL command tag (e.g. `SELECT`, `INSERT`, `UPDATE`, `DELETE`). |
| `fields` | array<object> | Column metadata for the result set. |
| `results` | array<object> | Results for each query in the batch, in order. |
| `rowAsArray` | boolean | Whether rows are returned as arrays (`true`) or objects (`false`). |
| `rowCount` | number | Number of rows affected by the command. |
| `rows` | array<string> | Result rows. Each row is an object (column-name keys) or an array (when array mode is enabled). |

## Native endpoint

Through the native Xata API, this operation is `POST /sql` (base URL `https://api.xata.tech`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/query.md) for the provider-specific parameters and requirements.

