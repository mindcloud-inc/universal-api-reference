# DocuProx: Create Processing Job



```
POST https://connect.mindcloud.co/v1/universal/docuProx/latest/actions/create-processing-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuProx `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/docuProx/latest/actions/create-processing-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "actualImage": "string",
  "templateId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docuProx/latest/actions/create-processing-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "actualImage": "string",
    "templateId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `actualImage` | file | yes | Base64-encoded image, uploaded file, or ZIP file containing documents. |
| `templateId` | string | yes | UUID of the DocuProx template to use. |
| `staticValues` | string | no | JSON string of static key-value pairs to include in the job response. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native DocuProx API returns.

## Native endpoint

Through the native DocuProx API, this operation is `POST /v1/process-job` (base URL `https://api.docuprox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-processing-job.md) for the provider-specific parameters and requirements.

