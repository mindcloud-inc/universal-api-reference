# Sisense: Delete Table Column

Deletes a column from a Sisense table.

```
DELETE https://connect.mindcloud.co/v1/universal/sisense/latest/actions/delete-table-column
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sisense `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/sisense/latest/actions/delete-table-column?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sisense/latest/actions/delete-table-column?${params}`, {
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
| `columns[].id` | string | no | The identifier of a column to keep after deletion. |
| `columns[].name` | string | no | The name of a column to keep after deletion. |
| `columns[].oid` | string | no | The oid of a column to keep after deletion. |
| `columns[].type` | string | no | The Sisense column type integer for a remaining column. |
| `datamodelId` | string | no | The Datamodel oid. |
| `datasetId` | string | no | The Dataset oid. |
| `tableId` | string | no | The Table oid. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Sisense API returns.

## Native endpoint

Through the native Sisense API, this operation is `PATCH /api/v2/datamodels/:datamodelId/datasets/:datasetId/tables/:tableId` (base URL `https://signup-126940n0.sisense.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-table-column.md) for the provider-specific parameters and requirements.

