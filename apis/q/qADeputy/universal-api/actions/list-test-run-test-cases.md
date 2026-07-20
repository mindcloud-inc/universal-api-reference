# QADeputy: List Test Run Test Cases

Retrieves test cases in a QADeputy test run.

```
GET https://connect.mindcloud.co/v1/universal/qADeputy/latest/actions/list-test-run-test-cases
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QADeputy `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/qADeputy/latest/actions/list-test-run-test-cases?connectionId=$CONNECTION_ID&limit=25&offset=0&testRunId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "testRunId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/qADeputy/latest/actions/list-test-run-test-cases?${params}`, {
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
| `testRunId` | number | yes | Required QADeputy test_run_id whose test cases should be listed. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actualResult": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "referenceId": "string",
      "testCaseId": 1,
      "testCaseStatus": "string",
      "testFeature": "string",
      "testFeatureId": 1,
      "testRunTestCaseId": 1,
      "testSuite": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actualResult` | string |  |
| `createdAt` | date |  |
| `name` | string |  |
| `referenceId` | string |  |
| `testCaseId` | number |  |
| `testCaseStatus` | string |  |
| `testFeature` | string |  |
| `testFeatureId` | number |  |
| `testRunTestCaseId` | number |  |
| `testSuite` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native QADeputy API, this operation is `GET /test-runs/:testRunId/test-cases` (base URL `https://app.qadeputy.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-test-run-test-cases.md) for the provider-specific parameters and requirements.

