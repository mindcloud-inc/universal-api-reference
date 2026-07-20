# Testlify: Get Candidate Result

Retrieves a candidate's assessment result from Testlify.

```
GET https://connect.mindcloud.co/v1/universal/testlify/latest/actions/get-candidate-result
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Testlify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/testlify/latest/actions/get-candidate-result?connectionId=$CONNECTION_ID&assessmentId=string&candidateId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "assessmentId": "string",
  "candidateId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/testlify/latest/actions/get-candidate-result?${params}`, {
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
| `assessmentId` | string | yes | Assessment identifier. |
| `candidateId` | string | yes | Candidate identifier. |
| `report` | string | no | Report type. |
| `fileType` | string | no | Export file format. |
| `testLibId` | string | no | Test library identifier for report selection. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assessmentCandidateId": "string",
      "assessmentCandidateUrl": "https://example.com",
      "assessmentId": "string",
      "assessmentName": "Ava Chen",
      "attemptIndex": 1,
      "avgScorePercentage": 1,
      "candidateId": "string",
      "candidateIndex": 1,
      "candidateStage": "string",
      "candidateStatus": "string",
      "completedAt": "string",
      "defaultLanguage": "string",
      "email": "ava@example.com",
      "firstName": "Ava",
      "invitedAt": "string",
      "isArchived": true,
      "lastName": "Chen",
      "orgId": "string",
      "orgName": "Ava Chen",
      "title": "string",
      "totalQuestion": 1,
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assessmentCandidateId` | string |  |
| `assessmentCandidateUrl` | string |  |
| `assessmentId` | string |  |
| `assessmentName` | string |  |
| `attemptIndex` | number |  |
| `avgScorePercentage` | number |  |
| `candidateId` | string |  |
| `candidateIndex` | number |  |
| `candidateStage` | string |  |
| `candidateStatus` | string |  |
| `completedAt` | string |  |
| `defaultLanguage` | string |  |
| `email` | string |  |
| `firstName` | string |  |
| `invitedAt` | string |  |
| `isArchived` | boolean |  |
| `lastName` | string |  |
| `orgId` | string |  |
| `orgName` | string |  |
| `title` | string |  |
| `totalQuestion` | number |  |
| `userId` | string |  |

## Native endpoint

Through the native Testlify API, this operation is `GET /v1/assessment/:assessmentId/candidate/:candidateId` (base URL `https://api.testlify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-candidate-result.md) for the provider-specific parameters and requirements.

