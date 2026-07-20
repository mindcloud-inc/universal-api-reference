# Appwrite: Create email

Creates a new email in your Appwrite project.

```
POST https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/messaging-create-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Appwrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/messaging-create-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "messageId": "string",
  "subject": "string",
  "content": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/messaging-create-email', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "messageId": "string",
    "subject": "string",
    "content": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `attachments` | string | no | Array of compound ID strings of bucket IDs and file IDs to be attached to the email. They should be formatted as <BUCKET_ID>:<FILE_ID>. |
| `bcc` | string | no | Array of target IDs to be added as BCC. |
| `cc` | string | no | Array of target IDs to be added as CC. |
| `messageId` | string | yes | Message ID. Choose a custom ID or generate a random ID with `ID.unique()`. Valid chars are a-z, A-Z, 0-9, period, hyphen, and underscore. Can't start with a special char. Max length is 36 chars. |
| `targets` | string | no | List of Targets IDs. |
| `topics` | string | no | List of Topic IDs. |
| `users` | string | no | List of User IDs. |
| `subject` | string | yes | Email Subject. |
| `content` | string | yes | Email Content. |
| `topics[]` | array<string> | no | List of Topic IDs. |
| `users[]` | array<string> | no | List of User IDs. |
| `targets[]` | array<string> | no | List of Targets IDs. |
| `cc[]` | array<string> | no | Array of target IDs to be added as CC. |
| `bcc[]` | array<string> | no | Array of target IDs to be added as BCC. |
| `attachments[]` | array<string> | no | Array of compound ID strings of bucket IDs and file IDs to be attached to the email. They should be formatted as <BUCKET_ID>:<FILE_ID>. |
| `draft` | boolean | no | Is message a draft |
| `html` | boolean | no | Is content of type HTML |
| `scheduledAt` | string | no | Scheduled delivery time for message in [ISO 8601](https://www.iso.org/iso-8601-date-and-time-format.html) format. DateTime value must be in future. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "$createdAt": "string",
      "$id": "string",
      "$updatedAt": "string",
      "data": {},
      "deliveredAt": "string",
      "deliveredTotal": 1,
      "deliveryErrors": [
        "string"
      ],
      "providerType": "string",
      "scheduledAt": "string",
      "status": "string",
      "targets": [
        "string"
      ],
      "topics": [
        "string"
      ],
      "users": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `$createdAt` | string | Message creation time in ISO 8601 format. |
| `$id` | string | Message ID. |
| `$updatedAt` | string | Message update date in ISO 8601 format. |
| `data` | object | Data of the message. |
| `deliveredAt` | string | The time when the message was delivered. |
| `deliveredTotal` | number | Number of recipients the message was delivered to. |
| `deliveryErrors` | array<string> | Delivery errors if any. |
| `providerType` | string | Message provider type. |
| `scheduledAt` | string | The scheduled time for message. |
| `status` | string | Status of delivery. |
| `targets` | array<string> | Target IDs set as recipients. |
| `topics` | array<string> | Topic IDs set as recipients. |
| `users` | array<string> | User IDs set as recipients. |

## Native endpoint

Through the native Appwrite API, this operation is `POST /messaging/messages/email` (base URL `https://cloud.appwrite.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/messaging-create-email.md) for the provider-specific parameters and requirements.

