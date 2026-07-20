# ContactOut: Queue Batch Email Verification

Creates a batch email verification job in ContactOut.

```
POST https://connect.mindcloud.co/v1/universal/contactOut/latest/actions/queue-batch-email-verification
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ContactOut `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/contactOut/latest/actions/queue-batch-email-verification" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "emails": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/contactOut/latest/actions/queue-batch-email-verification', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "emails": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `callback_url` | string | no | Optional callback URL for async bulk verification results. |
| `emails` | string | yes | An array of email addresses to verify in bulk. Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "job_id": "string",
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `job_id` | string |  |
| `message` | string |  |
| `status` | string |  |

## Native endpoint

Through the native ContactOut API, this operation is `POST /v1/email/verify/batch` (base URL `https://api.contactout.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/queue-batch-email-verification.md) for the provider-specific parameters and requirements.

