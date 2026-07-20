# MojoTxt: List Message Log

Retrieves a message log from MojoTxt.

```
GET https://connect.mindcloud.co/v1/universal/mojoTxt/latest/actions/list-message-log
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MojoTxt `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mojoTxt/latest/actions/list-message-log?connectionId=$CONNECTION_ID&limit=25&offset=0&phoneNumber=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "phoneNumber": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mojoTxt/latest/actions/list-message-log?${params}`, {
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
| `direction` | string | no | Filter the log to incoming (I) or outgoing (O) messages. |
| `endTime` | string | no | Show messages older than this UNIX timestamp. |
| `messageId` | string | no | Show log entries for a specific subscription-list message. |
| `phoneNumber` | string | yes | The MojoTxt phone number in international format, like +17792533748. |
| `startTime` | string | no | Show messages newer than this UNIX timestamp. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Body": "string",
      "Credits": 1,
      "DeliveryStatus": "string",
      "Direction": "string",
      "ErrorMessage": "string",
      "FirstName": "Ava",
      "LastName": "Chen",
      "LogID": 1,
      "Media": "string",
      "PhoneNumber": "string",
      "Timestamp": 1,
      "Type": "string",
      "URLClickTimestamp": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Body` | string | The text body of the message. |
| `Credits` | number | The number of MojoTxt credits consumed by the message. |
| `DeliveryStatus` | string | The carrier delivery status for outgoing messages. |
| `Direction` | string | Whether the message was incoming (I) or outgoing (O). |
| `ErrorMessage` | string | The human-readable delivery error, if any. |
| `FirstName` | string | The first name associated with the message contact. |
| `LastName` | string | The last name associated with the message contact. |
| `LogID` | number | The unique identifier for the message log record. |
| `Media` | string | The media URL for MMS messages, if present. |
| `PhoneNumber` | string | The phone number involved in the logged message. |
| `Timestamp` | number | The UNIX timestamp when the message was sent or received. |
| `Type` | string | The message type, either SMS or MMS. |
| `URLClickTimestamp` | number | The UNIX timestamp when the tracked URL was clicked, if present. |

## Native endpoint

Through the native MojoTxt API, this operation is `GET /:phoneNumber/messageLog/list` (base URL `https://app.mojotxt.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-message-log.md) for the provider-specific parameters and requirements.

