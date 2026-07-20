# Slack: List Scheduled Messages

Retrieves scheduled messages from a Slack workspace.

```
GET https://connect.mindcloud.co/v1/universal/slack/latest/actions/list-scheduled-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Slack `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/slack/latest/actions/list-scheduled-messages?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/slack/latest/actions/list-scheduled-messages?${params}`, {
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
| `channel` | list | no | Channel to send the message to. |
| `latest` | date | no | A Unix timestamp of the latest value in the time range |
| `oldest` | date | no | A Unix timestamp of the oldest value in the time range |

## Response

```json
{
  "success": true,
  "data": [
    {
      "channelId": "string",
      "dateCreated": 1,
      "id": "string",
      "postAt": 1,
      "text": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channelId` | string |  |
| `dateCreated` | number |  |
| `id` | string |  |
| `postAt` | number |  |
| `text` | string |  |

## Native endpoint

Through the native Slack API, this operation is `POST chat.scheduledMessages.list` (base URL `https://slack.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-scheduled-messages.md) for the provider-specific parameters and requirements.

