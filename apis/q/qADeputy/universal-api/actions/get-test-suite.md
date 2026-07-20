# QADeputy: Get Test Suite

Retrieves a test suite from QADeputy.

```
GET https://connect.mindcloud.co/v1/universal/qADeputy/latest/actions/get-test-suite
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QADeputy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/qADeputy/latest/actions/get-test-suite?connectionId=$CONNECTION_ID&testSuiteId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "testSuiteId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/qADeputy/latest/actions/get-test-suite?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "name": "Ava Chen",
      "product": "string",
      "productId": 1,
      "testCasesCount": 1,
      "testFeaturesCount": 1,
      "testSuiteId": 1,
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
| `description` | string |  |
| `name` | string |  |
| `product` | string |  |
| `productId` | number |  |
| `testCasesCount` | number |  |
| `testFeaturesCount` | number |  |
| `testSuiteId` | number |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native QADeputy API, this operation is `GET /test-suites/:testSuiteId` (base URL `https://app.qadeputy.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-test-suite.md) for the provider-specific parameters and requirements.

