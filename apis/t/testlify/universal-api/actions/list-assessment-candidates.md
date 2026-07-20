# Testlify: List Assessment Candidates

Retrieves candidates for a specific Testlify assessment.

```
GET https://connect.mindcloud.co/v1/universal/testlify/latest/actions/list-assessment-candidates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Testlify `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/testlify/latest/actions/list-assessment-candidates?connectionId=$CONNECTION_ID&limit=25&offset=0&assessmentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "assessmentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/testlify/latest/actions/list-assessment-candidates?${params}`, {
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
| `query` | string | no | Search query string. |
| `candidateStatus` | string | no | Filter by candidate status. |
| `candidateStage` | string | no | Filter by candidate stage. |
| `invitationType` | string | no | Filter by invitation type. |
| `grade` | string | no | Filter by grade. |
| `completedRange` | string | no | Filter by completion time range. |
| `invitedBy` | string | no | Filter by inviter. |
| `workspaceLabelTitle` | string | no | Filter by workspace label title. |
| `sortBy` | string | no | Column name to sort by. |
| `sortOrder` | string | no | Sort order. |
| `limit` | number | no | Number of items to return. |
| `skip` | number | no | Number of items to skip. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assessmentCandidateId": "string",
      "assessmentId": "string",
      "attemptIndex": 1,
      "avgScorePercentage": 1,
      "candidateId": "string",
      "candidateStage": "string",
      "candidateStatus": "string",
      "completedAt": "string",
      "email": "ava@example.com",
      "firstName": "Ava",
      "grading": "string",
      "gradingColor": "string",
      "invitedAt": "string",
      "invitedBy": "string",
      "invitedVia": "string",
      "lastName": "Chen",
      "numberOfAttempts": 1,
      "totalQuestion": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assessmentCandidateId` | string |  |
| `assessmentId` | string |  |
| `attemptIndex` | number |  |
| `avgScorePercentage` | number |  |
| `candidateId` | string |  |
| `candidateStage` | string |  |
| `candidateStatus` | string |  |
| `completedAt` | string |  |
| `email` | string |  |
| `firstName` | string |  |
| `grading` | string |  |
| `gradingColor` | string |  |
| `invitedAt` | string |  |
| `invitedBy` | string |  |
| `invitedVia` | string |  |
| `lastName` | string |  |
| `numberOfAttempts` | number |  |
| `totalQuestion` | number |  |

## Native endpoint

Through the native Testlify API, this operation is `GET /v1/assessment/:assessmentId/candidate` (base URL `https://api.testlify.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-assessment-candidates.md) for the provider-specific parameters and requirements.

