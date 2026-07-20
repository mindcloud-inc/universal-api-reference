# Slack: Delete Scheduled Message

Deletes a scheduled message from Slack.

```
DELETE https://connect.mindcloud.co/v1/universal/slack/latest/actions/delete-scheduled-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Slack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/slack/latest/actions/delete-scheduled-message?connectionId=$CONNECTION_ID&channel=string&scheduledMessageID=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "channel": "string",
  "scheduledMessageID": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/slack/latest/actions/delete-scheduled-message?${params}`, {
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
| `channel` | list | yes | The channel the message will be posted to |
| `scheduledMessageID` | list | yes | ID of the scheduled message |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `senderOverride` | list | no | Override the connection's Default Sender for this action only. One of: `bot`, `user`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ok": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ok` | boolean |  |

## Native endpoint

Through the native Slack API, this operation is `POST chat.deleteScheduledMessage` (base URL `https://slack.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-scheduled-message.md) for the provider-specific parameters and requirements.

