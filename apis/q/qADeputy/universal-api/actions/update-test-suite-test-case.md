# QADeputy: Update Test Suite Test Case

Updates a test case in a QADeputy test suite.

```
PUT https://connect.mindcloud.co/v1/universal/qADeputy/latest/actions/update-test-suite-test-case
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QADeputy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/qADeputy/latest/actions/update-test-suite-test-case" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "testSuiteId": 1,
  "testCaseId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/qADeputy/latest/actions/update-test-suite-test-case', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "testSuiteId": 1,
    "testCaseId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `testSuiteId` | number | yes | Required QADeputy test_suite_id. |
| `testCaseId` | number | yes | Required QADeputy test_case_id to update. |
| `name` | string | no | Updated test case name. |
| `preconditions` | string | no | Updated preconditions for the test case. |
| `expectedResults` | string | no | Updated expected results for the test case. |
| `testCaseSteps` | string | no | Updated test case steps. |
| `specifications` | string | no | Updated specifications URL or reference. |
| `time` | string | no | Estimated test case time in QADeputy's documented HH:mm format. Example: `23:12`. |

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

Through the native QADeputy API, this operation is `PUT /test-suites/:testSuiteId/test-cases/:testCaseId` (base URL `https://app.qadeputy.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-test-suite-test-case.md) for the provider-specific parameters and requirements.

