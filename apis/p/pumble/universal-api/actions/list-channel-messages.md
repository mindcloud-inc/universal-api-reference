# Pumble: List Channel Messages

Retrieves messages from a Pumble channel.

```
GET https://connect.mindcloud.co/v1/universal/pumble/latest/actions/list-channel-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pumble `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pumble/latest/actions/list-channel-messages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pumble/latest/actions/list-channel-messages?${params}`, {
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
| `channel` | string | no |  |
| `channelId` | string | no |  |
| `cursor` | string | no |  |
| `limit` | number | no |  |
| `strategy` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "hasMoreAfter": true,
      "hasMoreBefore": true,
      "messages": {
        "author": "string",
        "channelId": "string",
        "deleted": true,
        "edited": true,
        "id": "string",
        "isFollowing": true,
        "subtype": "string",
        "text": "string",
        "timestamp": "string",
        "timestampMilli": 1,
        "workspaceId": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `hasMoreAfter` | boolean |  |
| `hasMoreBefore` | boolean |  |
| `messages.author` | string |  |
| `messages.channelId` | string |  |
| `messages.deleted` | boolean |  |
| `messages.edited` | boolean |  |
| `messages.id` | string |  |
| `messages.isFollowing` | boolean |  |
| `messages.subtype` | string |  |
| `messages.text` | string |  |
| `messages.timestamp` | string |  |
| `messages.timestampMilli` | number |  |
| `messages.workspaceId` | string |  |

## Native endpoint

Through the native Pumble API, this operation is `GET /listMessages` (base URL `https://pumble-api-keys.addons.marketplace.cake.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-channel-messages.md) for the provider-specific parameters and requirements.

