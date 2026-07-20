# QADeputy: List Test Runs

Retrieves test runs from QADeputy.

```
GET https://connect.mindcloud.co/v1/universal/qADeputy/latest/actions/list-test-runs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QADeputy `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/qADeputy/latest/actions/list-test-runs?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/qADeputy/latest/actions/list-test-runs?${params}`, {
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
| `isCompleted` | list | no | Optional completion filter. Use 0 for active test runs and 1 for completed test runs; omit to list both. One of: `0`, `1`. |

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

Through the native QADeputy API, this operation is `GET /test-runs` (base URL `https://app.qadeputy.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-test-runs.md) for the provider-specific parameters and requirements.

