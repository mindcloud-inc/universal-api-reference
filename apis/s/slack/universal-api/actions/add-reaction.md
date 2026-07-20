# Slack: Add Reaction

Adds a reaction to an item in Slack.

```
POST https://connect.mindcloud.co/v1/universal/slack/latest/actions/add-reaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Slack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/slack/latest/actions/add-reaction" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "channel": "string",
  "timestamp": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/slack/latest/actions/add-reaction', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "channel": "string",
    "timestamp": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

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

Through the native Slack API, this operation is `POST reactions.add` (base URL `https://slack.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-reaction.md) for the provider-specific parameters and requirements.

