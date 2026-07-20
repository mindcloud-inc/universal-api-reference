# Sisense: Add Custom Column To Table

Adds a custom column to a Sisense table.

```
PUT https://connect.mindcloud.co/v1/universal/sisense/latest/actions/add-custom-column-to-table
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sisense `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sisense/latest/actions/add-custom-column-to-table" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sisense/latest/actions/add-custom-column-to-table', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `columns[].expression` | string | no | The SQL expression for the custom column. |
| `columns[].id` | string | no | The new custom column identifier. |
| `columns[].isCustom` | string | no | Set to true for the custom column. |
| `columns[].name` | string | no | The new custom column display name. |
| `columns[].oid` | string | no | The oid of an existing column to keep in the table payload. |
| `columns[].type` | string | no | The Sisense column type integer. |
| `datamodelId` | string | no | The Datamodel oid. |
| `datasetId` | string | no | The Dataset oid. |
| `tableId` | string | no | The Table oid. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Sisense API returns.

## Native endpoint

Through the native Sisense API, this operation is `PATCH /api/v2/datamodels/:datamodelId/datasets/:datasetId/tables/:tableId` (base URL `https://signup-126940n0.sisense.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-custom-column-to-table.md) for the provider-specific parameters and requirements.

