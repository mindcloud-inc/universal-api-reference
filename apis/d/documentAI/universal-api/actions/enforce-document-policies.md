# Document AI: Enforce Document Policies

Evaluates a document against policies in Document AI.

```
GET https://connect.mindcloud.co/v1/universal/documentAI/latest/actions/enforce-document-policies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Document AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/documentAI/latest/actions/enforce-document-policies?connectionId=$CONNECTION_ID&InputFile=string&Rules%5B%5D=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "InputFile": "string",
  "Rules[]": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/documentAI/latest/actions/enforce-document-policies?${params}`, {
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
| `InputFile` | string | yes | Base64-encoded document content to check against policy rules. |
| `Rules[]` | array<object> | yes | Policy rules to evaluate against the document. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `RecognitionMode` | string | no | OCR recognition mode. Default: `Advanced`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cleanResult": true,
      "riskScore": 1,
      "ruleViolations": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cleanResult` | boolean | Whether the document passed all policy checks. |
| `riskScore` | number | Overall policy risk score. |
| `ruleViolations` | array<object> | Policy rule violations found in the document. |

## Native endpoint

Through the native Document AI API, this operation is `POST /document-ai/document/analyze/enforce-policy` (base URL `https://api.cloudmersive.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/enforce-document-policies.md) for the provider-specific parameters and requirements.

