# Grist: Run SQL Query

Runs a SQL query in a Grist document.

```
GET https://connect.mindcloud.co/v1/universal/grist/latest/actions/run-sql-query
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Grist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/grist/latest/actions/run-sql-query?connectionId=$CONNECTION_ID&docId=string&sql=SELECT%20*%20FROM%20Table1%20LIMIT%2010" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "docId": "string",
  "sql": "SELECT * FROM Table1 LIMIT 10"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/grist/latest/actions/run-sql-query?${params}`, {
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
| `docId` | string | yes | Document ID |
| `sql` | string | yes | SQL query to execute Default: `SELECT * FROM Table1 LIMIT 10`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `timeout` | number | no | Query timeout in ms |

## Response

```json
{
  "success": true,
  "data": [
    {
      "statement": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `statement` | string |  |

## Native endpoint

Through the native Grist API, this operation is `POST /docs/:docId/sql` (base URL `https://docs.getgrist.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/run-sql-query.md) for the provider-specific parameters and requirements.

