# TestDome: Get Candidate

Retrieves a candidate from TestDome.

```
GET https://connect.mindcloud.co/v1/universal/testDome/latest/actions/get-candidate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TestDome `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/testDome/latest/actions/get-candidate?connectionId=$CONNECTION_ID&candidateId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "candidateId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/testDome/latest/actions/get-candidate?${params}`, {
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
| `candidateId` | number | yes |  |
| `expand` | list<string> | no |  |
| `select` | list<string> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_links": {},
      "activities": {},
      "anonymized": "string",
      "archived": true,
      "betterThan": {},
      "certificate": {},
      "deadline": "string",
      "email": "ava@example.com",
      "id": 1,
      "invitationKey": "string",
      "maxScore": 1,
      "name": "Ava Chen",
      "needsScoring": true,
      "notes": {},
      "passed": true,
      "passedOverride": true,
      "possibleCheating": true,
      "possibleCheatingAttempts": {},
      "proctoringEnabled": true,
      "proctoringStatus": "string",
      "questions": {},
      "score": 1,
      "shouldNotify": true,
      "skillScores": {},
      "status": "string",
      "tags": [
        "string"
      ],
      "test": {},
      "testUrl": {},
      "timeTaken": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_links` | object | Dictionary |
| `activities` | object | The activities associated with the candidate. |
| `anonymized` | string | The date when the candidate was anonymized. Remarks: Can be null if the candidate was not anonymized yet. |
| `archived` | boolean | Determines if the candidate is archived. |
| `betterThan` | object | The percentage of candidates that the current candidate outperforms. Remarks: If null , the candidate didn't finish the test yet. |
| `certificate` | object | The certificate associated with the candidate. Remarks: This can be null if the candidate doesn't have a certificate. |
| `deadline` | string | The deadline for the candidate to take the test. Remarks: Can be null if the candidate does not have a set deadline. |
| `email` | string | The email. |
| `id` | number | The ID of the candidate. |
| `invitationKey` | string | The unique invitation key. |
| `maxScore` | number | The potential max score of the candidate. Remarks: It will only have a value if it's not equal CandidateModel.Score . |
| `name` | string | The name of the candidate. |
| `needsScoring` | boolean | Determines if the candidate has answers that need to be manually scored. |
| `notes` | object | The notes associated with the candidate. |
| `passed` | boolean | Determines if the candidate has passed the test. Remarks: Always false if candidate has not finished the test yet. This property depends on the cutoff score and can also be overridden per candidate. Before using this property, check CandidateModel.PassedOverride . If that is null , the value of this property prevails. |
| `passedOverride` | boolean | Overrides the value of CandidateModel.Passed . Remarks: If it's null , no override has been applied and that value must be considered (ignoring this one). |
| `possibleCheating` | boolean | Determines if the candidate possibly cheated on its test. |
| `possibleCheatingAttempts` | object | The possible cheating attempts of the candidate. |
| `proctoringEnabled` | boolean | Determines if proctoring is enabled for the candidate. |
| `proctoringStatus` | string | The proctoring status of the candidate. |
| `questions` | object | The questions and answers associated with the candidate. |
| `score` | number | The score of the candidate. Remarks: If null , the candidate didn't finish the test yet. |
| `shouldNotify` | boolean | Determines if the candidate should be notified via email about its result in the test. |
| `skillScores` | object | The scores per skill of the candidate. |
| `status` | string | The status of the candidate. |
| `tags` | array<string> | The tags associated with the candidate. |
| `test` | object | The test that the candidate is invited to. |
| `testUrl` | object | The details of the Test URL used to invite the candidate. Remarks: It will be null if the candidate was not invited via a Test URL (invited via URL). |
| `timeTaken` | number | The time (in seconds) the candidate took to finish the test. Remarks: This is 0 if the candidate didn't finish the test yet. |

## Native endpoint

Through the native TestDome API, this operation is `GET /candidates/:candidateId` (base URL `https://api.staging.testdome.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-candidate.md) for the provider-specific parameters and requirements.

