# Resend: Send Batch Emails

Sends up to 100 emails in a Resend batch.

```
POST https://connect.mindcloud.co/v1/universal/resend/latest/actions/send-batch-emails
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Resend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/resend/latest/actions/send-batch-emails" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/resend/latest/actions/send-batch-emails', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



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
| `id` | string | The ID of the sent email. |

## Native endpoint

Through the native Resend API, this operation is `POST /emails/batch` (base URL `https://api.resend.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-batch-emails.md) for the provider-specific parameters and requirements.

