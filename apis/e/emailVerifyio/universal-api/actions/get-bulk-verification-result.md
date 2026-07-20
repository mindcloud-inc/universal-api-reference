# EmailVerify.io: Get Bulk Verification Result

Retrieves a bulk verification task result from EmailVerify.io.

```
GET https://connect.mindcloud.co/v1/universal/emailVerifyio/latest/actions/get-bulk-verification-result
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EmailVerify.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/emailVerifyio/latest/actions/get-bulk-verification-result?connectionId=$CONNECTION_ID&taskId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/emailVerifyio/latest/actions/get-bulk-verification-result?${params}`, {
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
| `taskId` | string | yes | Bulk verification task identifier returned when the task was created. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "countChecked": 1,
      "countTotal": 1,
      "name": "Ava Chen",
      "progressPercentage": 1,
      "results": {
        "emailBatch": [
          {
            "address": "ava@example.com",
            "status": "ava@example.com",
            "subStatus": "ava@example.com"
          }
        ]
      },
      "status": "string",
      "taskId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `countChecked` | number | How many emails have been checked. |
| `countTotal` | number | How many emails are in the task. |
| `name` | string | Bulk task title. |
| `progressPercentage` | number | Bulk task completion percentage. |
| `results.emailBatch[].address` | string | Email address included in the batch result. |
| `results.emailBatch[].status` | string | Verification status for that email address. |
| `results.emailBatch[].subStatus` | string | Detailed verification sub-status for that email address. |
| `status` | string | Current bulk task status. |
| `taskId` | number | Bulk verification task identifier. |

## Native endpoint

Through the native EmailVerify.io API, this operation is `GET /get-result-bulk-verification-task/` (base URL `https://app.emailverify.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-bulk-verification-result.md) for the provider-specific parameters and requirements.

