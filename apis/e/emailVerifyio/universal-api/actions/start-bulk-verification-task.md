# EmailVerify.io: Start Bulk Verification Task

Creates a bulk verification task in EmailVerify.io.

```
POST https://connect.mindcloud.co/v1/universal/emailVerifyio/latest/actions/start-bulk-verification-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EmailVerify.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/emailVerifyio/latest/actions/start-bulk-verification-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string",
  "emailBatch": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/emailVerifyio/latest/actions/start-bulk-verification-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string",
    "emailBatch": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | yes | Title for the bulk verification task. |
| `emailBatch` | object | yes | Array of email-address objects to verify in bulk. Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "countDuplicatesRemoved": 1,
      "countProcessing": 1,
      "countRejectedEmails": 1,
      "countSubmitted": 1,
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
| `countDuplicatesRemoved` | number | How many duplicate emails were removed. |
| `countProcessing` | number | How many emails are still processing. |
| `countRejectedEmails` | number | How many submitted emails were rejected. |
| `countSubmitted` | number | How many emails were submitted. |
| `status` | string | Queue status for the bulk verification task. |
| `taskId` | number | Bulk verification task identifier. |

## Native endpoint

Through the native EmailVerify.io API, this operation is `POST /validate-batch` (base URL `https://app.emailverify.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/start-bulk-verification-task.md) for the provider-specific parameters and requirements.

