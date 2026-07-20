# EndBounce: Verify Emails Batch

Creates a verification job in EndBounce for multiple emails.

```
POST https://connect.mindcloud.co/v1/universal/endBounce/latest/actions/verify-emails-batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EndBounce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/endBounce/latest/actions/verify-emails-batch" \
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
const response = await fetch('https://connect.mindcloud.co/v1/universal/endBounce/latest/actions/verify-emails-batch', {
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
| `emails[]` | array<string> | yes | Email addresses to verify in one batch request. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "mode": "string",
      "requestId": "string",
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Queue confirmation message. |
| `mode` | string | Response mode for the verification request. |
| `requestId` | string | Queued verification job request ID. |
| `total` | number | Number of emails accepted into the job. |

## Native endpoint

Through the native EndBounce API, this operation is `POST /v1/verify` (base URL `https://api.endbounce.com/api/integrations`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-emails-batch.md) for the provider-specific parameters and requirements.

