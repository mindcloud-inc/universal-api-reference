# Google Cloud Document AI: Review Document With Human Review Config

Creates a human review request in Google Cloud Document AI.

```
POST https://connect.mindcloud.co/v1/universal/googleCloudDocumentAI/latest/actions/review-document-with-human-review-config
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Cloud Document AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/googleCloudDocumentAI/latest/actions/review-document-with-human-review-config" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "processorsId": "string",
  "inlineDocument": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleCloudDocumentAI/latest/actions/review-document-with-human-review-config', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "processorsId": "string",
    "inlineDocument": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `processorsId` | string | yes | Document AI processor ID. |
| `inlineDocument` | object | yes | Document to send for human review. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `enableSchemaValidation` | boolean | no | Whether to validate the document against the schema. |
| `priority` | string | no | Review priority. |
| `documentSchema` | object | no | Optional schema to use for validation. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Google Cloud Document AI API returns.

## Native endpoint

Through the native Google Cloud Document AI API, this operation is `POST /v1/projects/:projectsId/locations/:locationsId/processors/:processorsId/humanReviewConfig:reviewDocument` (base URL `https://documentai.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/review-document-with-human-review-config.md) for the provider-specific parameters and requirements.

