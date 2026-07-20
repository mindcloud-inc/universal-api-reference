# Postmark: Send Batch Emails

Sends batch emails through Postmark.

```
POST https://connect.mindcloud.co/v1/universal/postmark/latest/actions/send-batch-emails
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Postmark `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/postmark/latest/actions/send-batch-emails" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/postmark/latest/actions/send-batch-emails', {
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
      "ErrorCode": 1,
      "Message": "string",
      "MessageID": "string",
      "SubmittedAt": "2026-05-07T12:00:00.000Z",
      "To": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ErrorCode` | number |  |
| `Message` | string |  |
| `MessageID` | string |  |
| `SubmittedAt` | date |  |
| `To` | string |  |

## Native endpoint

Through the native Postmark API, this operation is `POST /email/batch` (base URL `https://api.postmarkapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-batch-emails.md) for the provider-specific parameters and requirements.

