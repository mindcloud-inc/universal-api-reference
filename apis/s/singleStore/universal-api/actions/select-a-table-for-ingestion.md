# SingleStore: Select a Table for Ingestion

Updates whether a source table is selected for ingestion in SingleStore.

```
PUT https://connect.mindcloud.co/v1/universal/singleStore/latest/actions/select-a-table-for-ingestion
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SingleStore `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/singleStore/latest/actions/select-a-table-for-ingestion" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "database": "string",
  "schema": "string",
  "table": "string",
  "select": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/singleStore/latest/actions/select-a-table-for-ingestion', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "database": "string",
    "schema": "string",
    "table": "string",
    "select": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `database` | string | yes | Database name in the source system. |
| `schema` | string | yes | Schema name inside the selected database. |
| `table` | string | yes | Table name to update for ingestion. |
| `select` | string | yes | Whether the table should be selected for ingestion. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SingleStore API returns.

## Native endpoint

Through the native SingleStore API, this operation is `PATCH /config-tab/{database}/{schema}/{table}` (base URL `https://{{credentials.flowEndpoint}}:30081/ingest/api/ingest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/select-a-table-for-ingestion.md) for the provider-specific parameters and requirements.

