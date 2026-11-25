# Epicor Prophet 21: Query OData Table



```
GET https://connect.mindcloud.co/v1/universal/epicorProphet21/latest/actions/query-odata-table
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Epicor Prophet 21 `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/epicorProphet21/latest/actions/query-odata-table?connectionId=$CONNECTION_ID&limit=25&offset=0&tableName=supplier" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "tableName": "supplier"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/epicorProphet21/latest/actions/query-odata-table?${params}`, {
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
| `tableName` | list<string> | yes | Example: `supplier`. |
| `select` | string | no | Accepts multiple values in one string, delimited by `,`. Example: `supplier_id,supplier_name`. |
| `filter` | string | no | OData filter expression. Quote string values and double embedded single quotes. Combine values with or; do not use in, which can be silently ignored. Example: `supplier_id eq 10050`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `count` | boolean | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Epicor Prophet 21 API returns.

## Native endpoint

Through the native Epicor Prophet 21 API, this operation is `GET /odataservice/odata/table/:tableName` (base URL `{{credentials.apiUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/query-odata-table.md) for the provider-specific parameters and requirements.

