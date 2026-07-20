# Heymarket SMS: List Team Messages



```
GET https://connect.mindcloud.co/v1/universal/heymarketSMS/latest/actions/list-team-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Heymarket SMS `connectionId` ([setup](../authentication.md)).

This action also supports [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/heymarketSMS/latest/actions/list-team-messages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/heymarketSMS/latest/actions/list-team-messages?${params}`, {
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
| `createdAt` | string | no | Fetch messages created on and after this RFC 3339 timestamp. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "channel": "string",
      "conversation": {
        "assigned": 1,
        "blocked": true,
        "channel": "string",
        "created": "string",
        "emailNoti": true,
        "id": 1,
        "inbox": 1,
        "localId": "string",
        "members": {},
        "muted": true,
        "read": 1,
        "replied": true,
        "status": "string",
        "super": 1,
        "target": "string",
        "targets": {},
        "unread": true,
        "updated": "string"
      },
      "date": "string",
      "hidden": true,
      "id": 1,
      "localId": "string",
      "rawError": "string",
      "status": "string",
      "super": 1,
      "target": "string",
      "targetErrors": {
        "15555550123": "string"
      },
      "targets": {},
      "text": "string",
      "type": "string",
      "updated": "string",
      "user": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channel` | string |  |
| `conversation.assigned` | number |  |
| `conversation.blocked` | boolean |  |
| `conversation.channel` | string |  |
| `conversation.created` | string |  |
| `conversation.emailNoti` | boolean |  |
| `conversation.id` | number |  |
| `conversation.inbox` | number |  |
| `conversation.localId` | string |  |
| `conversation.members` | object |  |
| `conversation.muted` | boolean |  |
| `conversation.read` | number |  |
| `conversation.replied` | boolean |  |
| `conversation.status` | string |  |
| `conversation.super` | number |  |
| `conversation.target` | string |  |
| `conversation.targets` | object |  |
| `conversation.unread` | boolean |  |
| `conversation.updated` | string |  |
| `date` | string |  |
| `hidden` | boolean |  |
| `id` | number |  |
| `localId` | string |  |
| `rawError` | string |  |
| `status` | string |  |
| `super` | number |  |
| `target` | string |  |
| `targetErrors.15555550123` | string |  |
| `targets` | object |  |
| `text` | string |  |
| `type` | string |  |
| `updated` | string |  |
| `user` | number |  |

## Native endpoint

Through the native Heymarket SMS API, this operation is `POST /v1/messages/all` (base URL `https://api.heymarket.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-team-messages.md) for the provider-specific parameters and requirements.

