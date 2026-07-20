# Tally: List Form Submissions



```
GET https://connect.mindcloud.co/v1/universal/tally/latest/actions/list-form-submissions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tally `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tally/latest/actions/list-form-submissions?connectionId=$CONNECTION_ID&formId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "formId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tally/latest/actions/list-form-submissions?${params}`, {
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
| `formId` | list<string> | yes |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filter` | list<string> | no | Filter submissions by status |
| `startDate` | date | no | Filter submissions submitted on or after this date |
| `endDate` | date | no | Filter submissions submitted on or before this date |
| `afterId` | string | no | Get submissions that came after a specific submission ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "formId": "string",
      "id": "string",
      "isCompleted": true,
      "respondentId": "string",
      "responses": [
        {
          "answer": "string",
          "createdAt": "string",
          "formId": "string",
          "id": "string",
          "questionId": "string",
          "respondentId": "string",
          "sessionUuid": "string",
          "submissionId": "string",
          "updatedAt": "string"
        }
      ],
      "submittedAt": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `formId` | string |  |
| `id` | string |  |
| `isCompleted` | boolean |  |
| `respondentId` | string |  |
| `responses[].answer` | string |  |
| `responses[].createdAt` | string |  |
| `responses[].formId` | string |  |
| `responses[].id` | string |  |
| `responses[].questionId` | string |  |
| `responses[].respondentId` | string |  |
| `responses[].sessionUuid` | string |  |
| `responses[].submissionId` | string |  |
| `responses[].updatedAt` | string |  |
| `submittedAt` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Tally API, this operation is `GET forms/:formId/submissions` (base URL `https://api.tally.so`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-form-submissions.md) for the provider-specific parameters and requirements.

