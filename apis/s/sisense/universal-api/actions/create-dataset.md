# Sisense: Create Dataset

Creates a dataset in a Sisense datamodel.

```
POST https://connect.mindcloud.co/v1/universal/sisense/latest/actions/create-dataset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sisense `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sisense/latest/actions/create-dataset" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "datamodelId": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sisense/latest/actions/create-dataset', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "datamodelId": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `datamodelId` | string | yes | Datamodel OID. |
| `name` | string | yes | Dataset name. |
| `type` | string | no | Dataset type. Use custom for a connector-free dataset or extract for a connected dataset. Default: `custom`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `connection.oid` | string | no | Connection OID for extract datasets. |
| `database` | string | no | Database name for extract datasets when required by the connector. |
| `schemaName` | string | no | Schema name for extract datasets when required by the connector. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Sisense API returns.

## Native endpoint

Through the native Sisense API, this operation is `POST /api/v2/datamodels/:datamodelId/datasets` (base URL `https://signup-126940n0.sisense.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-dataset.md) for the provider-specific parameters and requirements.

