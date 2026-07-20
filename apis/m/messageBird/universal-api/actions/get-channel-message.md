# MessageBird: Get Channel Message



```
GET https://connect.mindcloud.co/v1/universal/messageBird/latest/actions/get-channel-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MessageBird `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/messageBird/latest/actions/get-channel-message?connectionId=$CONNECTION_ID&workspaceId=string&channelId=string&messageId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "string",
  "channelId": "string",
  "messageId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/messageBird/latest/actions/get-channel-message?${params}`, {
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
| `workspaceId` | string | yes | The Bird workspace ID that owns the channel. |
| `channelId` | string | yes | The Bird channel ID that owns the message. |
| `messageId` | string | yes | The Bird message ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "channelId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "details": "string",
      "direction": "string",
      "failure": {},
      "id": "string",
      "lastStatusAt": "2026-05-07T12:00:00.000Z",
      "meta": {},
      "origin": {},
      "parts": [
        {}
      ],
      "reason": "string",
      "receiver": "string",
      "reference": "string",
      "replyTo": {},
      "scheduledFor": "2026-05-07T12:00:00.000Z",
      "sender": "string",
      "shortLinks": {},
      "status": "string",
      "tags": [
        "string"
      ],
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channelId` | string |  |
| `createdAt` | date |  |
| `details` | string | This field is used to store additional information related to the message status. |
| `direction` | string |  |
| `failure` | object |  |
| `id` | string |  |
| `lastStatusAt` | date |  |
| `meta` | object |  |
| `origin` | object |  |
| `parts` | array<object> |  |
| `reason` | string |  |
| `receiver` | string |  |
| `reference` | string | A reference to the message. This can be used to identify the message in the channel. |
| `replyTo` | object |  |
| `scheduledFor` | date | Scheduled time to send message at. Must be formated as RFC3339 timestamp. When set, the message status will be `scheduled` until it's sent. Messages scheduled for a time in the past or within 10 minutes of the request may be sent immediately. Messages scheduled farther than 35 days will be rejected. |
| `sender` | string |  |
| `shortLinks` | object | SMS link shortening options. Must be included in the request for SMS channels when `enableLinkTracking` is set to true. When using templates, please refer to the template level `shortLinks` instead. |
| `status` | string |  |
| `tags` | array<string> | Tags to associate with the message. Tags are converted to lower case and tags that do not exist are automatically created. You can view your created tags in the UI. You can specify up to 10 tags per message. |
| `updatedAt` | date |  |

## Native endpoint

Through the native MessageBird API, this operation is `GET /workspaces/:workspaceId/channels/:channelId/messages/:messageId` (base URL `https://api.bird.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-channel-message.md) for the provider-specific parameters and requirements.

