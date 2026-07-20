# Document AI: Answer Document Questions



```
GET https://connect.mindcloud.co/v1/universal/documentAI/latest/actions/answer-document-questions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Document AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/documentAI/latest/actions/answer-document-questions?connectionId=$CONNECTION_ID&InputFile=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "InputFile": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/documentAI/latest/actions/answer-document-questions?${params}`, {
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
| `InputFile` | string | yes | Base64-encoded document content to answer questions from. |
| `QuestionsYesNo[]` | array<object> | no | Yes/no questions to answer from the document. |
| `QuestionsMultipleChoice[]` | array<object> | no | Multiple-choice questions to answer from the document. |
| `QuestionsFreeResponse[]` | array<object> | no | Free-response questions to answer from the document. |

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
      "answerResults": [
        {}
      ],
      "confidenceScore": 1,
      "successful": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `answerResults` | array<object> | Answers extracted from the document. |
| `confidenceScore` | number | Overall confidence score. |
| `successful` | boolean | Whether the question answering request succeeded. |

## Native endpoint

Through the native Document AI API, this operation is `POST /document-ai/document/analyze/answer-questions` (base URL `https://api.cloudmersive.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/answer-document-questions.md) for the provider-specific parameters and requirements.

