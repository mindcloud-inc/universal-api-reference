# Clarifai: Add Inputs To Dataset

Adds inputs to a dataset in Clarifai.

```
PUT https://connect.mindcloud.co/v1/universal/clarifai/latest/actions/add-inputs-to-dataset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clarifai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/clarifai/latest/actions/add-inputs-to-dataset" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "appId": "string",
  "datasetId": "string",
  "dataset_inputs[]": [
    {}
  ],
  "dataset_inputs[].input.id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clarifai/latest/actions/add-inputs-to-dataset', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "appId": "string",
    "datasetId": "string",
    "dataset_inputs[]": [{}],
    "dataset_inputs[].input.id": "string"
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
| `dataset_inputs[]` | array<object> | yes | Inputs to add to the dataset. |
| `dataset_inputs[].input` | object | no | Input reference. |
| `dataset_inputs[].input.id` | string | yes | Existing Clarifai input ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Clarifai API returns.

## Native endpoint

Through the native Clarifai API, this operation is `POST /v2/users/me/apps/:appId/datasets/:datasetId/inputs` (base URL `https://api.clarifai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-inputs-to-dataset.md) for the provider-specific parameters and requirements.

