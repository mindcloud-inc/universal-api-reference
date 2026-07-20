# Byteplant Email Validator: Create Bulk Email Validation Task

Creates a bulk email validation task in Byteplant Email Validator.

```
POST https://connect.mindcloud.co/v1/universal/byteplantEmailValidator/latest/actions/create-bulk-email-validation-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Byteplant Email Validator `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/byteplantEmailValidator/latest/actions/create-bulk-email-validation-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "emailsCsv": "Email\nsupport@byteplant.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/byteplantEmailValidator/latest/actions/create-bulk-email-validation-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "emailsCsv": "Email\nsupport@byteplant.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `emailsCsv` | string | yes | CSV content with an `Email` header and one email address per row. Example: `Email support@byteplant.com`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `taskName` | string | no | Optional name for the bulk validation task. Example: `March list cleanup`. |
| `validationMode` | list | no | Optional validation mode. Express retries unavailable servers for 2 hours; extensive retries for 72 hours. One of: `express`, `extensive`. Default: `express`. |
| `notifyEmail` | string | no | Optional email address to receive completion notifications for this task. Example: `ops@example.com`. |
| `notifyUrl` | string | no | Optional URL to receive a completion notification with the task id. Example: `https://example.com/byteplant-callback`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "info": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `info` | string | Task identifier when accepted, or provider error information when the request is rejected. |
| `status` | number | Byteplant bulk validation result code. `121` means the task was accepted; `119` indicates an input or API error. |

## Native endpoint

Through the native Byteplant Email Validator API, this operation is `POST /api/bulk-verify` (base URL `https://api.email-validator.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-bulk-email-validation-task.md) for the provider-specific parameters and requirements.

