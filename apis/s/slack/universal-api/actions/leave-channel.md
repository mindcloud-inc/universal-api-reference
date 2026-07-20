# Slack: Leave Channel

Leaves an existing conversation in Slack.

```
DELETE https://connect.mindcloud.co/v1/universal/slack/latest/actions/leave-channel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Slack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/slack/latest/actions/leave-channel?connectionId=$CONNECTION_ID&channel=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "channel": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/slack/latest/actions/leave-channel?${params}`, {
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
| `channel` | list<string> | yes | Conversation to leave |
| `sendAsBot` | boolean | no | Determines if this action should be performed by the current user or the Mindcloud bot. Default: `true`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Slack API returns.

## Native endpoint

Through the native Slack API, this operation is `POST conversations.leave` (base URL `https://slack.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/leave-channel.md) for the provider-specific parameters and requirements.

