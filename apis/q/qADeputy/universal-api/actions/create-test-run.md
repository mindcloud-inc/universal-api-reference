# QADeputy: Create Test Run

Creates a new test run in QADeputy.

```
POST https://connect.mindcloud.co/v1/universal/qADeputy/latest/actions/create-test-run
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QADeputy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/qADeputy/latest/actions/create-test-run" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "testSuite": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/qADeputy/latest/actions/create-test-run', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "testSuite": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Test run name. |
| `description` | string | no | Test run description. |
| `testSuite` | number | yes | QADeputy test suite ID to create the test run from. |
| `users[]` | array<number> | no | QADeputy user IDs assigned to the test run. |
| `includeAll` | boolean | no | Whether QADeputy should include all test cases. Default: `false`. |
| `testCases[]` | array<number> | no | QADeputy test case IDs to include when includeAll is false. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completedAt": "2026-05-07T12:00:00.000Z",
      "completedTestCasesCount": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "failedTestCasesCount": 1,
      "name": "Ava Chen",
      "notTestingCasesCount": 1,
      "passedTestCasesCount": 1,
      "productId": 1,
      "productName": "Ava Chen",
      "testRunId": 1,
      "testRunMode": "string",
      "testRunStatus": "string",
      "testSuiteId": 1,
      "testSuiteName": "Ava Chen",
      "timeRemaining": "string",
      "totalTestCasesCount": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completedAt` | date |  |
| `completedTestCasesCount` | number |  |
| `createdAt` | date |  |
| `description` | string |  |
| `failedTestCasesCount` | number |  |
| `name` | string |  |
| `notTestingCasesCount` | number |  |
| `passedTestCasesCount` | number |  |
| `productId` | number |  |
| `productName` | string |  |
| `testRunId` | number |  |
| `testRunMode` | string |  |
| `testRunStatus` | string |  |
| `testSuiteId` | number |  |
| `testSuiteName` | string |  |
| `timeRemaining` | string |  |
| `totalTestCasesCount` | number |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native QADeputy API, this operation is `POST /test-runs` (base URL `https://app.qadeputy.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-test-run.md) for the provider-specific parameters and requirements.

