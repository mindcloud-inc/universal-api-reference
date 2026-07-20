# QADeputy: Create Test Result

Creates a test result for a QADeputy test case.

```
POST https://connect.mindcloud.co/v1/universal/qADeputy/latest/actions/create-test-result
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QADeputy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/qADeputy/latest/actions/create-test-result" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "testCaseId": 1,
  "testCaseStatus": 1,
  "createdByUserId": 1,
  "testRun": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/qADeputy/latest/actions/create-test-result', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "testCaseId": 1,
    "testCaseStatus": 1,
    "createdByUserId": 1,
    "testRun": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `testCaseId` | number | yes | Required QADeputy test_case_id receiving a test result. |
| `testCaseStatus` | number | yes | QADeputy test case status ID/value for the result. |
| `actualResult` | string | no | Actual result notes. |
| `createdByUserId` | number | yes | QADeputy user ID creating the result. |
| `testRun` | number | yes | QADeputy test run ID for the result. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actualResult": "string",
      "createdBy": "string",
      "testCaseId": "string",
      "testCaseName": "Ava Chen",
      "testCaseStatus": "string",
      "testRun": {
        "name": "Ava Chen",
        "testRunId": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actualResult` | string |  |
| `createdBy` | string |  |
| `testCaseId` | string |  |
| `testCaseName` | string |  |
| `testCaseStatus` | string |  |
| `testRun.name` | string |  |
| `testRun.testRunId` | number |  |

## Native endpoint

Through the native QADeputy API, this operation is `POST /test-cases/:testCaseId/test-results` (base URL `https://app.qadeputy.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-test-result.md) for the provider-specific parameters and requirements.

