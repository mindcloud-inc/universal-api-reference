# Sisense: Get Dataset

Retrieves a dataset from a Sisense datamodel.

```
GET https://connect.mindcloud.co/v1/universal/sisense/latest/actions/get-dataset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sisense `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sisense/latest/actions/get-dataset?connectionId=$CONNECTION_ID&datamodelId=string&datasetId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "datamodelId": "string",
  "datasetId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sisense/latest/actions/get-dataset?${params}`, {
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
| `datamodelId` | string | yes |  |
| `datasetId` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Sisense API returns.

## Native endpoint

Through the native Sisense API, this operation is `GET /api/v2/datamodels/:datamodelId/datasets/:datasetId` (base URL `https://signup-126940n0.sisense.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-dataset.md) for the provider-specific parameters and requirements.

