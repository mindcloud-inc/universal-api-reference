# MojoTxt: List Messages

Retrieves messages for a MojoTxt phone number.

```
GET https://connect.mindcloud.co/v1/universal/mojoTxt/latest/actions/list-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MojoTxt `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mojoTxt/latest/actions/list-messages?connectionId=$CONNECTION_ID&limit=25&offset=0&phoneNumber=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "phoneNumber": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mojoTxt/latest/actions/list-messages?${params}`, {
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
| `listId` | string | no | Return only messages sent to a specific list. |
| `phoneNumber` | string | yes | The MojoTxt phone number in international format, like +17792533748. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "LinksClicked": 1,
      "Media": "string",
      "Message": "string",
      "MessageID": 1,
      "MessagesSent": 1,
      "PublishTime": 1,
      "ScheduleType": "string",
      "Sent": 1,
      "Type": "string",
      "URL": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `LinksClicked` | number | The number of recipients who clicked the tracked link when stats are included. |
| `Media` | string | The media URL for MMS messages, if present. |
| `Message` | string | The body of the message. |
| `MessageID` | number | The unique identifier for the subscription list message. |
| `MessagesSent` | number | The number of recipients who were sent the message when stats are included. |
| `PublishTime` | number | The UNIX timestamp when the message is scheduled to be sent or was sent. |
| `ScheduleType` | string | Whether the message is scheduled at a specific time or relative to subscription time. |
| `Sent` | number | The send status code for the message. |
| `Type` | string | The message type, either SMS or MMS. |
| `URL` | string | The tracked URL appended to the message, if present. |

## Native endpoint

Through the native MojoTxt API, this operation is `GET /:phoneNumber/messages/list` (base URL `https://app.mojotxt.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-messages.md) for the provider-specific parameters and requirements.

