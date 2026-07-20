# Slack: Kick User From Channel

Removes a user from a Slack conversation.

```
DELETE https://connect.mindcloud.co/v1/universal/slack/latest/actions/kick-user-from-channel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Slack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/slack/latest/actions/kick-user-from-channel?connectionId=$CONNECTION_ID&channel=string&user=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "channel": "string",
  "user": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/slack/latest/actions/kick-user-from-channel?${params}`, {
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
| `channel` | list | yes | ID of conversation to remove user from. |
| `user` | list | yes | User ID to be removed. |
| `sendAsBot` | boolean | no | Determines if this action should be performed by the current user or the Mindcloud bot. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error": {},
      "errors": {},
      "ok": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error` | object |  |
| `errors` | object |  |
| `ok` | boolean |  |

## Native endpoint

Through the native Slack API, this operation is `POST conversations.kick` (base URL `https://slack.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/kick-user-from-channel.md) for the provider-specific parameters and requirements.

