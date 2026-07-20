# Sisense: Delete Dataset

Deletes an existing dataset from Sisense.

```
DELETE https://connect.mindcloud.co/v1/universal/sisense/latest/actions/delete-dataset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sisense `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/sisense/latest/actions/delete-dataset?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sisense/latest/actions/delete-dataset?${params}`, {
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
| `datamodelId` | string | no | The Datamodel oid. |
| `datasetId` | string | no | The Dataset oid. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Sisense API returns.

## Native endpoint

Through the native Sisense API, this operation is `DELETE /api/v2/datamodels/:datamodelId/datasets/:datasetId` (base URL `https://signup-126940n0.sisense.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-dataset.md) for the provider-specific parameters and requirements.

