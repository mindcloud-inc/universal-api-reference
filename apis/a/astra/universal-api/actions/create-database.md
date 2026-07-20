# Astra: Create Database

Creates a new database in Astra.

```
POST https://connect.mindcloud.co/v1/universal/astra/latest/actions/create-database
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Astra `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/astra/latest/actions/create-database" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "cloudProvider": "string",
  "name": "Ava Chen",
  "region": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/astra/latest/actions/create-database', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "cloudProvider": "string",
    "name": "Ava Chen",
    "region": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `capacityUnits` | number | no | Capacity units for the database. The verified workflow in this buildout uses 1. Default: `1`. |
| `cloudProvider` | string | yes | The cloud provider, such as AWS, GCP, or AZURE. |
| `dbType` | string | no | The database type. The verified workflow in this buildout uses vector. Default: `vector`. |
| `keyspace` | string | no | Optional keyspace name. Leave empty to use Astra's default keyspace for vector databases. |
| `name` | string | yes | The database name. |
| `region` | string | yes | The deployment region. |
| `tier` | string | no | The Astra tier. The verified workflow in this buildout uses serverless. Default: `serverless`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Astra API returns.

## Native endpoint

Through the native Astra API, this operation is `POST /v2/databases` (base URL `https://api.astra.datastax.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-database.md) for the provider-specific parameters and requirements.

