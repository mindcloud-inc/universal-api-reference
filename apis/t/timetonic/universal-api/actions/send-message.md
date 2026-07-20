# Timetonic: Send Message

Creates a new message in Timetonic.

```
POST https://connect.mindcloud.co/v1/universal/timetonic/latest/actions/send-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timetonic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/timetonic/latest/actions/send-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "message": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/timetonic/latest/actions/send-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "message": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `message` | string | yes | Message text to send. |
| `bookCode` | string | no | Optional code of the book that will receive the message. |
| `bookOwner` | string | no | Optional owner of the book that will receive the message. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `messageId` | string | no | Optional message id when editing an existing message. |
| `body` | string | no | Optional message body payload. |
| `event` | string | no | Optional event value associated with the message. |
| `uuid` | string | no | Optional client UUID for the message. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": 1,
      "createdVNB": "string",
      "createMessageId": 1,
      "req": "string",
      "sstamp": 1,
      "status": "string",
      "transactionId": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | number | Unix timestamp for message creation. |
| `createdVNB` | string | TimeTonic backend version string. |
| `createMessageId` | number | Identifier of the created message. |
| `req` | string | Echoed provider request name. |
| `sstamp` | number | Provider sync stamp after the message send. |
| `status` | string | Provider status for the message send request. |
| `transactionId` | string | Provider transaction identifier for the request. |
| `uuid` | string | Provider UUID for the created message. |

## Native endpoint

Through the native Timetonic API, this operation is `POST` (base URL `https://timetonic.com/live/api.php`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-message.md) for the provider-specific parameters and requirements.

