# Sisense: Create Relation

Creates a relation in a Sisense datamodel.

```
POST https://connect.mindcloud.co/v1/universal/sisense/latest/actions/create-relation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sisense `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sisense/latest/actions/create-relation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "datamodelId": "string",
  "columns[0].dataset": "string",
  "columns[0].table": "string",
  "columns[0].column": "string",
  "columns[1].dataset": "string",
  "columns[1].table": "string",
  "columns[1].column": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sisense/latest/actions/create-relation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "datamodelId": "string",
    "columns[0].dataset": "string",
    "columns[0].table": "string",
    "columns[0].column": "string",
    "columns[1].dataset": "string",
    "columns[1].table": "string",
    "columns[1].column": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `datamodelId` | string | yes |  |
| `columns[0].dataset` | string | yes |  |
| `columns[0].table` | string | yes |  |
| `columns[0].column` | string | yes |  |
| `columns[1].dataset` | string | yes |  |
| `columns[1].table` | string | yes |  |
| `columns[1].column` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Sisense API returns.

## Native endpoint

Through the native Sisense API, this operation is `POST /api/v2/datamodels/:datamodelId/relations` (base URL `https://signup-126940n0.sisense.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-relation.md) for the provider-specific parameters and requirements.

