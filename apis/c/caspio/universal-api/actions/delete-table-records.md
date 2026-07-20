# Caspio: Delete Table Records

Deletes existing table records from Caspio.

```
DELETE https://connect.mindcloud.co/v1/universal/caspio/latest/actions/delete-table-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Caspio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/caspio/latest/actions/delete-table-records?connectionId=$CONNECTION_ID&tableName=Ava%20Chen&where=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tableName": "Ava Chen",
  "where": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/caspio/latest/actions/delete-table-records?${params}`, {
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
| `where` | string | yes | SQL-like WHERE clause that selects the rows to delete. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Caspio API returns.

## Native endpoint

Through the native Caspio API, this operation is `DELETE /v3/tables/{tableName}/records` (base URL `https://d2hbw900.caspio.com/integrations/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-table-records.md) for the provider-specific parameters and requirements.

