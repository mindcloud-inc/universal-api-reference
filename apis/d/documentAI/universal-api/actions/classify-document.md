# Document AI: Classify Document

Classifies a document using Document AI.

```
GET https://connect.mindcloud.co/v1/universal/documentAI/latest/actions/classify-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Document AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/documentAI/latest/actions/classify-document?connectionId=$CONNECTION_ID&InputFile=string&Categories=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "InputFile": "string",
  "Categories": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/documentAI/latest/actions/classify-document?${params}`, {
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
| `InputFile` | file | yes | Document file to classify. |
| `Categories` | string | yes | Comma-separated document categories sent as the Cloudmersive Categories header. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `recognitionMode` | string | no | Optional recognition mode sent as a request header. Default: `Advanced`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "confidenceScore": 1,
      "documentCategoryResult": "string",
      "successful": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `confidenceScore` | number | Classification confidence score. |
| `documentCategoryResult` | string | Best matching document category. |
| `successful` | boolean | Whether document classification succeeded. |

## Native endpoint

Through the native Document AI API, this operation is `POST /document-ai/document/extract/classify` (base URL `https://api.cloudmersive.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/classify-document.md) for the provider-specific parameters and requirements.

