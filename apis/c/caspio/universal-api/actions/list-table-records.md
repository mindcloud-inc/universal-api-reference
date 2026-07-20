# Caspio: List Table Records

Retrieves all table records from Caspio.

```
GET https://connect.mindcloud.co/v1/universal/caspio/latest/actions/list-table-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Caspio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/caspio/latest/actions/list-table-records?connectionId=$CONNECTION_ID&tableName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tableName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/caspio/latest/actions/list-table-records?${params}`, {
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
| `tableName` | string | yes | Target table name. |
| `limit` | number | no | Maximum rows to return. |
| `pageNumber` | number | no | Page number. |
| `pageSize` | number | no | Rows per page. |
| `getPaginationInfo` | boolean | no | Set true to include pagination metadata. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `select` | string | no | Comma-separated field list. |
| `where` | string | no | SQL-like WHERE clause. |
| `groupBy` | string | no | SQL-like GROUP BY clause. |
| `orderBy` | string | no | SQL-like ORDER BY clause. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Caspio API returns.

## Native endpoint

Through the native Caspio API, this operation is `GET /v3/tables/{tableName}/records` (base URL `https://d2hbw900.caspio.com/integrations/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-table-records.md) for the provider-specific parameters and requirements.

