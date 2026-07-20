# MailFloss: Create Batch Verification Job

Creates a batch email verification job in MailFloss.

```
POST https://connect.mindcloud.co/v1/universal/mailFloss/latest/actions/create-batch-verification-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailFloss `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mailFloss/latest/actions/create-batch-verification-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "emails[]": [
    "ava@example.com"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailFloss/latest/actions/create-batch-verification-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "emails[]": ["ava@example.com"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `emails[]` | array<string> | yes | Email addresses to verify in the batch job. |
| `webhookUrl` | string | no | Optional webhook URL to receive results when the job completes. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Returned batch verification job ID. |

## Native endpoint

Through the native MailFloss API, this operation is `POST /batch-verify` (base URL `https://api.mailfloss.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-batch-verification-job.md) for the provider-specific parameters and requirements.

