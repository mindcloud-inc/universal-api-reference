# QADeputy: Update Test Run Test Case

Updates a test case in a QADeputy test run.

```
PUT https://connect.mindcloud.co/v1/universal/qADeputy/latest/actions/update-test-run-test-case
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QADeputy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/qADeputy/latest/actions/update-test-run-test-case" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "testRunId": 1,
  "testCaseId": 1,
  "testCaseStatus": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/qADeputy/latest/actions/update-test-run-test-case', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "testRunId": 1,
    "testCaseId": 1,
    "testCaseStatus": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `testRunId` | number | yes | Required QADeputy test_run_id. |
| `testCaseId` | number | yes | Required QADeputy test_case_id in the test run. |
| `testCaseStatus` | number | yes | QADeputy test case status ID/value for this run test case. |
| `actualResult` | string | no | Actual result notes for the test case in this run. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "previousValue": [
        {
          "actualResult": "string",
          "testCaseStatus": 1
        }
      ],
      "updatedValue": [
        {
          "actualResult": "string",
          "testCaseStatus": 1
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `previousValue[].actualResult` | string |  |
| `previousValue[].testCaseStatus` | number |  |
| `updatedValue[].actualResult` | string |  |
| `updatedValue[].testCaseStatus` | number |  |

## Native endpoint

Through the native QADeputy API, this operation is `PUT /test-runs/:testRunId/test-cases/:testCaseId` (base URL `https://app.qadeputy.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-test-run-test-case.md) for the provider-specific parameters and requirements.

