# Sisense: Create Table

Creates a table in a Sisense dataset.

```
POST https://connect.mindcloud.co/v1/universal/sisense/latest/actions/create-table
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sisense `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sisense/latest/actions/create-table" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "datamodelId": "string",
  "datasetId": "string",
  "id": "mc_stage3_table",
  "name": "MindCloud Stage3 Table",
  "type": "custom",
  "expression": "select 1 as id"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sisense/latest/actions/create-table', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "datamodelId": "string",
    "datasetId": "string",
    "id": "mc_stage3_table",
    "name": "MindCloud Stage3 Table",
    "type": "custom",
    "expression": "select 1 as id"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `datamodelId` | string | yes |  |
| `datasetId` | string | yes |  |
| `id` | string | yes | Example: `mc_stage3_table`. |
| `name` | string | yes | Example: `MindCloud Stage3 Table`. |
| `type` | string | yes | Default: `custom`. |
| `expression` | string | yes | Example: `select 1 as id`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Sisense API returns.

## Native endpoint

Through the native Sisense API, this operation is `POST /api/v2/datamodels/:datamodelId/datasets/:datasetId/tables` (base URL `https://signup-126940n0.sisense.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-table.md) for the provider-specific parameters and requirements.

