# QADeputy: List Test Case Statuses

Retrieves test case statuses from QADeputy.

```
GET https://connect.mindcloud.co/v1/universal/qADeputy/latest/actions/list-test-case-statuses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QADeputy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/qADeputy/latest/actions/list-test-case-statuses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/qADeputy/latest/actions/list-test-case-statuses?${params}`, {
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
| `statusType` | list | no | Optional test case status type filter. The docs use predefined_status. One of: `0`. Default: `predefined_status`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "colorCode": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "isComplete": 1,
      "name": "Ava Chen",
      "testCaseStatusId": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `colorCode` | string |  |
| `createdAt` | date |  |
| `description` | string |  |
| `isComplete` | number |  |
| `name` | string |  |
| `testCaseStatusId` | number |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native QADeputy API, this operation is `GET /test-case-statuses` (base URL `https://app.qadeputy.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-test-case-statuses.md) for the provider-specific parameters and requirements.

