# Google Cloud Document AI: Set Default Processor Version

Sets the default processor version in Google Cloud Document AI.

```
PUT https://connect.mindcloud.co/v1/universal/googleCloudDocumentAI/latest/actions/set-default-processor-version
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Cloud Document AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/googleCloudDocumentAI/latest/actions/set-default-processor-version" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "processorsId": "string",
  "defaultProcessorVersion": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleCloudDocumentAI/latest/actions/set-default-processor-version', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "processorsId": "string",
    "defaultProcessorVersion": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `processorsId` | string | yes | Document AI processor ID. |
| `defaultProcessorVersion` | string | yes | Full resource name of the processor version to set as default. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Google Cloud Document AI API returns.

## Native endpoint

Through the native Google Cloud Document AI API, this operation is `POST /v1/projects/:projectsId/locations/:locationsId/processors/:processorsId:setDefaultProcessorVersion` (base URL `https://documentai.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-default-processor-version.md) for the provider-specific parameters and requirements.

