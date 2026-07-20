# Slack: Send User Message

Creates a new direct message in Slack.

```
POST https://connect.mindcloud.co/v1/universal/slack/latest/actions/send-user-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Slack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/slack/latest/actions/send-user-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "channel": "string",
  "text": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/slack/latest/actions/send-user-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "channel": "string",
    "text": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `channel` | list | yes | Slack user to send the message to. |
| `text` | string | yes | The content of the message. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `senderOverride` | list | no | Override the connection's Default Sender for this action only. One of: `bot`, `user`. |
| `username` | string | no | Set your bot's user name. |
| `iconEmoji` | string | no | Emoji to use as the icon for this message. Overrides Icon Url. |
| `iconURL` | string | no | URL to an image to use as the icon for this message. |
| `unfurlLinks` | boolean | no | Pass true to enable unfurling of primarily text-based content. Default: `true`. |
| `unfurlMedia` | boolean | no | Pass false to disable unfurling of media content. Default: `true`. |
| `parse` | list | no | By default, URLs will be hyperlinked. Set parse to none to remove the hyperlinks. The behavior of parse is different for text formatted with markdown. By default, or when parse is set to none, markdown formatting is implemented. To ignore markdown formatting, set parse to full. |
| `mrkdwn` | boolean | no | Disable Slack markup parsing by setting to false. Enabled by default. Default: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "channel": "string",
      "message": {
        "appId": "string",
        "blocks": [
          {
            "blockId": "string",
            "elements": [
              {
                "elements": [
                  {
                    "text": "string",
                    "type": "string"
                  }
                ],
                "type": "string"
              }
            ],
            "type": "string"
          }
        ],
        "botId": "string",
        "botProfile": {
          "appId": "string",
          "deleted": true,
          "icons": {
            "image36": "string",
            "image48": "string",
            "image72": "string"
          },
          "id": "string",
          "name": "Ava Chen",
          "teamId": "string",
          "updated": 1
        },
        "team": "string",
        "text": "string",
        "ts": "string",
        "type": "string",
        "user": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channel` | string |  |
| `message.appId` | string |  |
| `message.blocks[].blockId` | string |  |
| `message.blocks[].elements[].elements[].text` | string |  |
| `message.blocks[].elements[].elements[].type` | string |  |
| `message.blocks[].elements[].type` | string |  |
| `message.blocks[].type` | string |  |
| `message.botId` | string |  |
| `message.botProfile.appId` | string |  |
| `message.botProfile.deleted` | boolean |  |
| `message.botProfile.icons.image36` | string |  |
| `message.botProfile.icons.image48` | string |  |
| `message.botProfile.icons.image72` | string |  |
| `message.botProfile.id` | string |  |
| `message.botProfile.name` | string |  |
| `message.botProfile.teamId` | string |  |
| `message.botProfile.updated` | number |  |
| `message.team` | string |  |
| `message.text` | string |  |
| `message.ts` | string |  |
| `message.type` | string |  |
| `message.user` | string |  |

## Native endpoint

Through the native Slack API, this operation is `POST chat.postMessage` (base URL `https://slack.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-user-message.md) for the provider-specific parameters and requirements.

