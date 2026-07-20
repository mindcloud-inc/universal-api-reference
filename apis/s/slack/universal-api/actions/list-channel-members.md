# Slack: List Channel Members

Retrieves conversation members from a Slack workspace.

```
GET https://connect.mindcloud.co/v1/universal/slack/latest/actions/list-channel-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Slack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/slack/latest/actions/list-channel-members?connectionId=$CONNECTION_ID&channel=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "channel": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/slack/latest/actions/list-channel-members?${params}`, {
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
| `channel` | list<string> | yes | ID of the conversation to retrieve members for. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sendAsBot` | boolean | no | Determines if this action should be performed by the current user or the Mindcloud bot. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Slack user ID of a channel member. |

## Native endpoint

Through the native Slack API, this operation is `GET conversations.members` (base URL `https://slack.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-channel-members.md) for the provider-specific parameters and requirements.

