# DocuPipe: Retrieve Detailed Processing Result

Retrieves detailed processing results from DocuPipe.

```
GET https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/retrieve-detailed-processing-result
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuPipe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/retrieve-detailed-processing-result?connectionId=$CONNECTION_ID&documentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "documentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/retrieve-detailed-processing-result?${params}`, {
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
| `documentId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "documentId": "string",
      "handwriting": true,
      "language": "string",
      "pages": [
        {}
      ],
      "plaintext": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `documentId` | string | Unique identifier for the document |
| `handwriting` | boolean | True if the document contains handwriting |
| `language` | string | Language of the document, e.g. en, fr, etc. |
| `pages` | array<object> | List of parsed pages with detailed information on word level location |
| `plaintext` | string | A textual representation of the entire document. This representation preserves the spatial arrangement of information in the document. It is designed to be both human-readable and LLM-redable. You can use this representation to prompt your own AI engines and build complex workflows around it. |

## Native endpoint

Through the native DocuPipe API, this operation is `GET /document/:documentId/detailed` (base URL `https://app.docupipe.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-detailed-processing-result.md) for the provider-specific parameters and requirements.

