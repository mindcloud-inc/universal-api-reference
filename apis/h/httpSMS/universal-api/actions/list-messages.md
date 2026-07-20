# httpSMS: List Messages



```
GET https://connect.mindcloud.co/v1/universal/httpSMS/latest/actions/list-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a httpSMS `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/httpSMS/latest/actions/list-messages?connectionId=$CONNECTION_ID&limit=25&offset=0&owner=string&contact=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "owner": "string",
  "contact": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/httpSMS/latest/actions/list-messages?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `owner` | string | yes | The owner's phone number. |
| `contact` | string | yes | The contact's phone number. |
| `query` | string | no | Filter messages containing this query. |
| `limit` | number | no | Number of messages to return. |
| `skip` | number | no | Number of messages to skip. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attachments": [
        "string"
      ],
      "contact": "string",
      "content": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "deliveredAt": "2026-05-07T12:00:00.000Z",
      "encrypted": true,
      "expiredAt": "2026-05-07T12:00:00.000Z",
      "failedAt": "2026-05-07T12:00:00.000Z",
      "failureReason": "string",
      "id": "string",
      "lastAttemptedAt": "2026-05-07T12:00:00.000Z",
      "maxSendAttempts": 1,
      "orderTimestamp": "2026-05-07T12:00:00.000Z",
      "owner": "string",
      "receivedAt": "2026-05-07T12:00:00.000Z",
      "requestId": "string",
      "requestReceivedAt": "2026-05-07T12:00:00.000Z",
      "scheduledAt": "2026-05-07T12:00:00.000Z",
      "scheduledSendTime": "2026-05-07T12:00:00.000Z",
      "sendAttemptCount": 1,
      "sendTime": 1,
      "sentAt": "2026-05-07T12:00:00.000Z",
      "sim": "string",
      "status": "string",
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attachments` | array<string> | Attachment URLs sent with the message. |
| `contact` | string | The contact phone number for the message thread. |
| `content` | string | The SMS or MMS message content. |
| `createdAt` | date | When the message record was created. |
| `deliveredAt` | date | When the message was delivered to the recipient. |
| `encrypted` | boolean | Whether the message content is end-to-end encrypted. |
| `expiredAt` | date | When the message expired before sending. |
| `failedAt` | date | When the message send failed. |
| `failureReason` | string | The provider failure reason when the message did not send. |
| `id` | string | The unique message ID. |
| `lastAttemptedAt` | date | When the system last attempted to send the message. |
| `maxSendAttempts` | number | The maximum number of send attempts allowed. |
| `orderTimestamp` | date | The ordering timestamp used for message sorting. |
| `owner` | string | The owner phone number used for the message. |
| `receivedAt` | date | When the device received the message. |
| `requestId` | string | The client-supplied request ID, when provided. |
| `requestReceivedAt` | date | When the API request was received by httpSMS. |
| `scheduledAt` | date | When the message was scheduled. |
| `scheduledSendTime` | date | The scheduled send time in the profile timezone. |
| `sendAttemptCount` | number | How many send attempts have been made. |
| `sendTime` | number | The send duration in nanoseconds. |
| `sentAt` | date | When the phone sent the message. |
| `sim` | string | The SIM slot used to send the message. |
| `status` | string | The current message status. |
| `type` | string | The message type. |
| `updatedAt` | date | When the message record was last updated. |
| `userId` | string | The owning user ID. |

## Native endpoint

Through the native httpSMS API, this operation is `GET /messages` (base URL `https://api.httpsms.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-messages.md) for the provider-specific parameters and requirements.

