# Tricentis qTest: List Test Logs

Retrieves test logs from Tricentis qTest.

```
GET https://connect.mindcloud.co/v1/universal/tricentisQTest/latest/actions/list-test-logs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tricentis qTest `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tricentisQTest/latest/actions/list-test-logs?connectionId=$CONNECTION_ID&projectId=1&testRunId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "1",
  "testRunId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tricentisQTest/latest/actions/list-test-logs?${params}`, {
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
| `projectId` | number | yes | ID of the qTest project. |
| `testRunId` | number | yes | ID of the Test Run. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "exe_end_date": "2026-05-07T12:00:00.000Z",
      "exe_start_date": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "note": "string",
      "status": {},
      "test_case_version_id": 1,
      "test_step_logs": [
        {}
      ],
      "user_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `exe_end_date` | date |  |
| `exe_start_date` | date |  |
| `id` | number |  |
| `note` | string |  |
| `status` | object |  |
| `test_case_version_id` | number |  |
| `test_step_logs` | array<object> |  |
| `user_id` | number |  |

## Native endpoint

Through the native Tricentis qTest API, this operation is `GET /projects/{projectId}/test-runs/{testRunId}/test-logs` (base URL `https://mindcloudapps.qtestnet.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-test-logs.md) for the provider-specific parameters and requirements.

