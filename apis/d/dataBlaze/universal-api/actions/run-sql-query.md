# Data Blaze: Run SQL Query

Runs a SQL query in Data Blaze.

```
GET https://connect.mindcloud.co/v1/universal/dataBlaze/latest/actions/run-sql-query
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Data Blaze `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dataBlaze/latest/actions/run-sql-query?connectionId=$CONNECTION_ID&query=SELECT%20Name%2C%20Count%20FROM%20Mindcloud" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "SELECT Name, Count FROM Mindcloud"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dataBlaze/latest/actions/run-sql-query?${params}`, {
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
| `query` | string | yes | BSQL query to run inside the Data Blaze space. Example: `SELECT Name, Count FROM Mindcloud`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "results": [
        {}
      ],
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `results` | array<object> | Rows returned by the BSQL query. |
| `status` | string | Query execution status from Data Blaze. |

## Native endpoint

Through the native Data Blaze API, this operation is `POST /api/database/1OzRoKyYgXpIR32FUO1JMm/query/` (base URL `https://data-api.blaze.today`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/run-sql-query.md) for the provider-specific parameters and requirements.

