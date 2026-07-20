# Send Channel Message with Slack

Creates a new message in a Slack channel.

## Endpoint

- **Method:** `POST`
- **Path:** `chat.postMessage`
- **Base URL:** `https://slack.com/api/`
- **Official documentation:** [Send Channel Message](https://docs.slack.dev/reference/methods/chat.postMessage/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channel` | body | `list` | yes | Slack channel to send the message to. Maximum length: 0. |
| `text` | body | `string` | yes | The content of the message. |
| `senderOverride` | body | `list` | no | Override the connection's Default Sender for this action only. Accepted values: `bot`, `user`. |
| `username` | body | `string` | no | Set your bot's user name. |
| `icon_emoji` | body | `string` | no | Emoji to use as the icon for this message. Overrides Icon Url. |
| `icon_url` | body | `string` | no | URL to an image to use as the icon for this message. |
| `unfurl_links` | body | `boolean` | no | Pass true to enable unfurling of primarily text-based content. Format: `toggle`. |
| `unfurl_media` | body | `boolean` | no | Pass false to disable unfurling of media content. Format: `toggle`. |
| `parse` | body | `list` | no | By default, URLs will be hyperlinked. Set parse to none to remove the hyperlinks.  The behavior of parse is different for text formatted with markdown. By default, or when parse is set to none, markdown formatting is implemented. To ignore markdown formatting, set parse to full. |
| `mrkdwn` | body | `boolean` | no | Disable Slack markup parsing by setting to false. Enabled by default. Format: `toggle`. |
| `thread_ts` | body | `list` | no | Provide another message's timestamp value to make this message a reply. Avoid using a reply's timestamp value; use its parent instead. |
| `reply_broadcast` | body | `boolean` | no | Used in conjunction with Thread Timestamp and indicates whether reply should be made visible to everyone in the channel or conversation. Format: `toggle`. |
