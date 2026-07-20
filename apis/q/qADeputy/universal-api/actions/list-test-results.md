# QADeputy: List Test Results

Retrieves test results for a QADeputy test case.

```
GET https://connect.mindcloud.co/v1/universal/qADeputy/latest/actions/list-test-results
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QADeputy `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/qADeputy/latest/actions/list-test-results?connectionId=$CONNECTION_ID&limit=25&offset=0&testCaseId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "testCaseId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/qADeputy/latest/actions/list-test-results?${params}`, {
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
| `testCaseId` | number | yes | Required QADeputy test_case_id whose results should be listed. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actualResult": "string",
      "createdBy": "string",
      "testCaseId": 1,
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
| `testCaseId` | number |  |
| `testCaseName` | string |  |
| `testCaseStatus` | string |  |
| `testRun.name` | string |  |
| `testRun.testRunId` | number |  |

## Native endpoint

Through the native QADeputy API, this operation is `GET /test-cases/:testCaseId/test-results` (base URL `https://app.qadeputy.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-test-results.md) for the provider-specific parameters and requirements.

