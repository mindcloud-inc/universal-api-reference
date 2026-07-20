# Slack: Remove Reaction

Removes a reaction from an item in Slack.

```
DELETE https://connect.mindcloud.co/v1/universal/slack/latest/actions/remove-reaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Slack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/slack/latest/actions/remove-reaction?connectionId=$CONNECTION_ID&channel=string&timestamp=string&name=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "channel": "string",
  "timestamp": "string",
  "name": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/slack/latest/actions/remove-reaction?${params}`, {
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
| `channel` | list<string> | yes | Channel where the message to add reaction to was posted. |
| `timestamp` | list<string> | yes | Timestamp of the message to add reaction to. |
| `name` | string | yes | Reaction (emoji) name. Ex: thumbsup |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `senderOverride` | list | no | Override the connection's Default Sender for this action only. One of: `bot`, `user`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Slack API returns.

## Native endpoint

Through the native Slack API, this operation is `POST reactions.remove` (base URL `https://slack.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-reaction.md) for the provider-specific parameters and requirements.

