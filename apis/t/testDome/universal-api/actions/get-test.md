# TestDome: Get Test

Retrieves a test from TestDome.

```
GET https://connect.mindcloud.co/v1/universal/testDome/latest/actions/get-test
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TestDome `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/testDome/latest/actions/get-test?connectionId=$CONNECTION_ID&testId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "testId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/testDome/latest/actions/get-test?${params}`, {
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
| `expand` | list<string> | no |  |
| `select` | list<string> | no |  |
| `testId` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_links": {},
      "affectedByNextDeprecation": true,
      "archived": true,
      "candidatesCount": {},
      "created": "string",
      "cutoffScore": 1,
      "daysUntilNextDeprecation": 1,
      "description": "string",
      "expectedPassRate": {},
      "id": 1,
      "inviteViaEmailParameters": {},
      "name": "Ava Chen",
      "needsScoring": 1,
      "notifyCandidatesParameters": {},
      "notifyTo": [
        "string"
      ],
      "owner": {},
      "proctoringConsent": true,
      "questions": {},
      "questionsCount": {},
      "scheduledCandidatesCount": {},
      "skills": {},
      "testUrls": {},
      "testUrlStatus": "https://example.com",
      "timeLimit": {},
      "urlSettings": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_links` | object | Dictionary |
| `affectedByNextDeprecation` | boolean | Indicates if the test is affected by the next question deprecation wave. |
| `archived` | boolean | The flag to describe if the test is archived. |
| `candidatesCount` | object | The total of candidates in this test. |
| `created` | string | The date of creation. |
| `cutoffScore` | number | Minimum score for a candidate to be considered approved. Range is [0, 100]. |
| `daysUntilNextDeprecation` | number | Indicates how many days until the next question deprecation wave. Note that this test will only be affected if TestModel.AffectedByNextDeprecation is `true`. |
| `description` | string | The description (plain text). |
| `expectedPassRate` | object | The percentage of candidates expected to pass this test considering the current questions. |
| `id` | number | The ID. |
| `inviteViaEmailParameters` | object | The last parameters used to invite a candidate via email in this test. |
| `name` | string | The name. |
| `needsScoring` | number | Returns the number of candidates that need scoring. If null, the test does not have manually scored questions. |
| `notifyCandidatesParameters` | object | The last parameters used to notify candidate's passing status via email in this test. |
| `notifyTo` | array<string> | Defines the email addresses of those that will be notified when a candidate finishes this test. |
| `owner` | object | The owner (author) of this test. |
| `proctoringConsent` | boolean | Indicates if the consent to enable proctoring was provided. Remarks: The value can be: - true : the consent request was given and it shouldn't be requested on the next invitation. - false : the consent request wasn't given or was denied and it should be requested on the next invitation. |
| `questions` | object | The questions that make up this test. |
| `questionsCount` | object | The total of questions in this test. |
| `scheduledCandidatesCount` | object | The total of scheduled candidates in this test. |
| `skills` | object | The skills of the questions of this test. |
| `testUrls` | object | The URLs used to share this test. |
| `testUrlStatus` | string | The status of the test URL(s) in this test. none: Test has no URL(s) created. on: Test has URL(s) available for candidates to take the test. off: Test has URL(s) created but none is available for candidates to take the test. |
| `timeLimit` | object | The time limit of all the questions in this test. |
| `urlSettings` | object | The URL settings of this test. |

## Native endpoint

Through the native TestDome API, this operation is `GET /tests/:testId` (base URL `https://api.staging.testdome.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-test.md) for the provider-specific parameters and requirements.

