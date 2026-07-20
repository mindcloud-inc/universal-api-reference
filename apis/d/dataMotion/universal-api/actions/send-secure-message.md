# DataMotion: Send Secure Message

Sends a secure message through DataMotion.

```
POST https://connect.mindcloud.co/v1/universal/dataMotion/latest/actions/send-secure-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DataMotion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dataMotion/latest/actions/send-secure-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "from": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dataMotion/latest/actions/send-secure-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "from": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `from` | string | yes | Email address of the DataMotion user sending the secure message. |
| `to[]` | array<string> | no | Recipients of the secure message. Accepts multiple values as an array. |
| `subject` | string | no | Subject of the secure message. |
| `textBody` | string | no | Plain text body of the secure message. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cc[]` | array<string> | no | Recipients copied on the secure message. Accepts multiple values as an array. |
| `bcc[]` | array<string> | no | Recipients blind-copied on the secure message. Accepts multiple values as an array. |
| `htmlBody` | string | no | HTML body of the secure message. |
| `attachments[]` | array<object> | no | Array of attachment objects with AttachmentBase64, ContentType, FileName, and optional ContentId. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ApplicationId": "string",
      "Expiration": "2026-05-07T12:00:00.000Z",
      "MessageSize": 1,
      "NumberOfRecipients": 1,
      "ProjectId": "string",
      "TransactionId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ApplicationId` | string | DataMotion application identifier. |
| `Expiration` | date | Message expiration date/time. |
| `MessageSize` | number | Message size in bytes. |
| `NumberOfRecipients` | number | Total recipient count. |
| `ProjectId` | string | DataMotion project identifier. |
| `TransactionId` | string | Transaction identifier for the sent secure message. |

## Native endpoint

Through the native DataMotion API, this operation is `POST /v1.2/Email` (base URL `https://api.datamotion.com/SecureMessageDelivery`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-secure-message.md) for the provider-specific parameters and requirements.

