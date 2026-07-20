# Google Cloud Document AI: Train Processor Version

Trains a processor version in Google Cloud Document AI.

```
POST https://connect.mindcloud.co/v1/universal/googleCloudDocumentAI/latest/actions/train-processor-version
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Cloud Document AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/googleCloudDocumentAI/latest/actions/train-processor-version" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "processorsId": "string",
  "processorVersion": {},
  "inputData": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleCloudDocumentAI/latest/actions/train-processor-version', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "processorsId": "string",
    "processorVersion": {},
    "inputData": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `processorsId` | string | yes | Document AI processor ID. |
| `processorVersion` | object | yes | Processor version configuration to train. |
| `inputData` | object | yes | Training input data configuration. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `documentSchema` | object | no | Document schema used for training. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Google Cloud Document AI API returns.

## Native endpoint

Through the native Google Cloud Document AI API, this operation is `POST /v1/projects/:projectsId/locations/:locationsId/processors/:processorsId/processorVersions:train` (base URL `https://documentai.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/train-processor-version.md) for the provider-specific parameters and requirements.

