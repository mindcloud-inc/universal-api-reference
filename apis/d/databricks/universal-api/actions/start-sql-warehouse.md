# Databricks: Start SQL Warehouse

Starts a SQL warehouse in the Databricks workspace.

```
PUT https://connect.mindcloud.co/v1/universal/databricks/latest/actions/start-sql-warehouse
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Databricks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/databricks/latest/actions/start-sql-warehouse" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "warehouseId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/databricks/latest/actions/start-sql-warehouse', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "warehouseId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `warehouseId` | string | yes | Required. Id of the SQL warehouse. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cluster_size": "string",
      "id": "string",
      "name": "Ava Chen",
      "state": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cluster_size` | string | Configured cluster size. |
| `id` | string | Unique identifier for the warehouse. |
| `name` | string | Logical warehouse name. |
| `state` | string | Current warehouse state. |

## Native endpoint

Through the native Databricks API, this operation is `POST {{credentials.host}}/api/2.0/sql/warehouses/:warehouseId/start` (base URL `https://accounts.cloud.databricks.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/start-sql-warehouse.md) for the provider-specific parameters and requirements.

