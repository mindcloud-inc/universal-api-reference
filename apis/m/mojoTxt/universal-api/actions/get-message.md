# MojoTxt: Get Message

Retrieves a message from MojoTxt.

```
GET https://connect.mindcloud.co/v1/universal/mojoTxt/latest/actions/get-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MojoTxt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mojoTxt/latest/actions/get-message?connectionId=$CONNECTION_ID&messageId=string&phoneNumber=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "messageId": "string",
  "phoneNumber": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mojoTxt/latest/actions/get-message?${params}`, {
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
| `messageId` | string | yes | The message identifier to retrieve. |
| `phoneNumber` | string | yes | The MojoTxt phone number in international format, like +17792533748. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Attach": "string",
      "Filters": [
        "string"
      ],
      "HTML": "string",
      "LinksClicked": 1,
      "Lists": [
        1
      ],
      "Media": "string",
      "Message": "string",
      "MessageID": 1,
      "MessagesSent": 1,
      "PublishTime": 1,
      "Recipients": [
        "string"
      ],
      "ScheduleType": "string",
      "SendAfter": 1,
      "SendAfterUnit": "string",
      "Sent": 1,
      "StatusMessage": "string",
      "Type": "string",
      "URL": "https://example.com",
      "UserID": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Attach` | string | The attachment payload, if present. |
| `Filters` | array<string> | The filters applied to the message audience. |
| `HTML` | string | The HTML version of the message, if present. |
| `LinksClicked` | number | The number of recipients who clicked the tracked link. |
| `Lists` | array<number> | The subscription list IDs targeted by the message. |
| `Media` | string | The media URL for MMS messages, if present. |
| `Message` | string | The body of the message. |
| `MessageID` | number | The unique identifier for the message. |
| `MessagesSent` | number | The number of recipients who were sent the message. |
| `PublishTime` | number | The UNIX timestamp when the message is scheduled to be sent or was sent. |
| `Recipients` | array<string> | The explicit recipients for the message, if present. |
| `ScheduleType` | string | Whether the message is scheduled at a specific time or relative to subscription time. |
| `SendAfter` | number | The delay interval used for relative scheduling, if present. |
| `SendAfterUnit` | string | The unit for the relative delay, if present. |
| `Sent` | number | The send status code for the message. |
| `StatusMessage` | string | The provider status message, if present. |
| `Type` | string | The message type, either SMS or MMS. |
| `URL` | string | The tracked URL appended to the message, if present. |
| `UserID` | number | The owner user identifier for the message, if present. |

## Native endpoint

Through the native MojoTxt API, this operation is `GET /:phoneNumber/messages/get/:messageId` (base URL `https://app.mojotxt.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-message.md) for the provider-specific parameters and requirements.

