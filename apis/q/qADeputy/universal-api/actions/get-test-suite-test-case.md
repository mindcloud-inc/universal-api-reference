# QADeputy: Get Test Suite Test Case

Retrieves a test case from a QADeputy test suite.

```
GET https://connect.mindcloud.co/v1/universal/qADeputy/latest/actions/get-test-suite-test-case
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QADeputy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/qADeputy/latest/actions/get-test-suite-test-case?connectionId=$CONNECTION_ID&testSuiteId=1&testCaseId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "testSuiteId": "1",
  "testCaseId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/qADeputy/latest/actions/get-test-suite-test-case?${params}`, {
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
| `testSuiteId` | number | yes | Required QADeputy test_suite_id. |
| `testCaseId` | number | yes | Required QADeputy test_case_id. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "deletedAt": "string",
      "expectedResults": "string",
      "lastRunTime": "string",
      "name": "Ava Chen",
      "preconditions": "string",
      "referenceId": "string",
      "specifications": "string",
      "testCaseId": 1,
      "testCaseSteps": "string",
      "testFeature": "string",
      "testFeatureId": 1,
      "testSuite": "string",
      "time": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `deletedAt` | string |  |
| `expectedResults` | string |  |
| `lastRunTime` | string |  |
| `name` | string |  |
| `preconditions` | string |  |
| `referenceId` | string |  |
| `specifications` | string |  |
| `testCaseId` | number |  |
| `testCaseSteps` | string |  |
| `testFeature` | string |  |
| `testFeatureId` | number |  |
| `testSuite` | string |  |
| `time` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native QADeputy API, this operation is `GET /test-suites/:testSuiteId/test-cases/:testCaseId` (base URL `https://app.qadeputy.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-test-suite-test-case.md) for the provider-specific parameters and requirements.

