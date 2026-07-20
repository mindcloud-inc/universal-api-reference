# Clarifai: Create Dataset Version

Creates a dataset version in Clarifai.

```
POST https://connect.mindcloud.co/v1/universal/clarifai/latest/actions/create-dataset-version
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clarifai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/clarifai/latest/actions/create-dataset-version" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "appId": "string",
  "datasetId": "string",
  "dataset_versions[]": [
    {}
  ],
  "dataset_versions[].id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clarifai/latest/actions/create-dataset-version', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "appId": "string",
    "datasetId": "string",
    "dataset_versions[]": [{}],
    "dataset_versions[].id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `appId` | string | yes | Clarifai app ID. |
| `datasetId` | string | yes | Clarifai dataset ID. |
| `dataset_versions[]` | array<object> | yes | Dataset versions to create. |
| `dataset_versions[].id` | string | yes | Dataset version ID. |
| `dataset_versions[].description` | string | no | Dataset version description. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Clarifai API returns.

## Native endpoint

Through the native Clarifai API, this operation is `POST /v2/users/me/apps/:appId/datasets/:datasetId/versions` (base URL `https://api.clarifai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-dataset-version.md) for the provider-specific parameters and requirements.

