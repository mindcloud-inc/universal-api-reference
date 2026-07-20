# Maildrip: Upload attachment To An Email



```
POST https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/upload-attachment-to-an-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Maildrip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/upload-attachment-to-an-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "emailId": "ava@example.com",
  "attachment": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/upload-attachment-to-an-email', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "emailId": "ava@example.com",
    "attachment": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `emailId` | string | yes | ID of the email to upload the attachment to |
| `attachment` | file | yes | The attachment file to upload (Max 50kb) |

## Response

```json
{
  "success": true,
  "data": [
    {
      "filename": "Ava Chen",
      "id": "string",
      "location": "string",
      "src": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `filename` | string |  |
| `id` | string |  |
| `location` | string |  |
| `src` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Maildrip API, this operation is `POST /api/v1/attachments/{email_id}` (base URL `https://api.maildrip.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-attachment-to-an-email.md) for the provider-specific parameters and requirements.

