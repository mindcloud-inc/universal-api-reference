# Testlify: Get Question

Retrieves a specific question from Testlify by ID.

```
GET https://connect.mindcloud.co/v1/universal/testlify/latest/actions/get-question
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Testlify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/testlify/latest/actions/get-question?connectionId=$CONNECTION_ID&questionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "questionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/testlify/latest/actions/get-question?${params}`, {
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
| `questionId` | string | yes | Question identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "answerSelectionType": "string",
      "checkedForGrammar": true,
      "classification": "string",
      "created": "string",
      "difficultyLevel": "string",
      "enableTestCase": true,
      "format": "string",
      "hasCorrectAnswer": true,
      "isMandatory": true,
      "isPreviewQuestion": true,
      "isScorableQuestion": true,
      "language": "string",
      "maximumScore": 1,
      "modified": "string",
      "question": "string",
      "recordingTime": 1,
      "reviewerStatus": "string",
      "score": 1,
      "showTypingResultToCandidate": true,
      "skill": "string",
      "skillId": "string",
      "source": "string",
      "sourceId": 1,
      "status": "string",
      "testLibraryId": "string",
      "testLibraryTitle": "string",
      "timeLimit": 1,
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string |  |
| `answerSelectionType` | string |  |
| `checkedForGrammar` | boolean |  |
| `classification` | string |  |
| `created` | string |  |
| `difficultyLevel` | string |  |
| `enableTestCase` | boolean |  |
| `format` | string |  |
| `hasCorrectAnswer` | boolean |  |
| `isMandatory` | boolean |  |
| `isPreviewQuestion` | boolean |  |
| `isScorableQuestion` | boolean |  |
| `language` | string |  |
| `maximumScore` | number |  |
| `modified` | string |  |
| `question` | string |  |
| `recordingTime` | number |  |
| `reviewerStatus` | string |  |
| `score` | number |  |
| `showTypingResultToCandidate` | boolean |  |
| `skill` | string |  |
| `skillId` | string |  |
| `source` | string |  |
| `sourceId` | number |  |
| `status` | string |  |
| `testLibraryId` | string |  |
| `testLibraryTitle` | string |  |
| `timeLimit` | number |  |
| `title` | string |  |

## Native endpoint

Through the native Testlify API, this operation is `GET /v1/question/:questionId` (base URL `https://api.testlify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-question.md) for the provider-specific parameters and requirements.

