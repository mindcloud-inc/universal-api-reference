# PDF-app: Analyze File With AI

Retrieves AI analysis from a file in PDF-app.

```
GET https://connect.mindcloud.co/v1/universal/pDFApp/latest/actions/analyze-file-with-ai
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PDF-app `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pDFApp/latest/actions/analyze-file-with-ai?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pDFApp/latest/actions/analyze-file-with-ai?${params}`, {
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
| `input_text` | string | no | Instruction or question for the AI analyzer. Example: `Summarize the attached file in three bullet points.`. |
| `fileUrl[]` | array<string> | no | Optional file URLs to analyze alongside the prompt. Example: `https://www.w3.org/WAI/ER/tests/xhtml/testfiles/resources/pdf/dummy.pdf`. |
| `examples` | string | no | Optional extra examples or guidance for the AI model. Example: `Focus on invoice totals and due dates.`. |
| `async` | boolean | no | Whether to run the AI analysis asynchronously. Default: `false`. |
| `type` | string | no | Model selector such as model1, model2, or model3. Example: `model2`. |
| `temperature` | number | no | Controls response variability between 0 and 1. Example: `0.2`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native PDF-app API returns.

## Native endpoint

Through the native PDF-app API, this operation is `POST /ai` (base URL `https://api.pdf-app.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/analyze-file-with-ai.md) for the provider-specific parameters and requirements.

