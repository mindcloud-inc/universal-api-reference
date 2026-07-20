# Pumble: Get Channel

Retrieves a channel from Pumble by ID or name.

```
GET https://connect.mindcloud.co/v1/universal/pumble/latest/actions/get-channel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pumble `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pumble/latest/actions/get-channel?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pumble/latest/actions/get-channel?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "channel": {
        "channelType": "string",
        "description": "string",
        "id": "string",
        "isArchived": true,
        "isHidden": true,
        "isMain": true,
        "isMember": true,
        "lastMessageTimestamp": "string",
        "name": "Ava Chen",
        "timestamp": "string",
        "workspaceId": "string"
      },
      "users": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channel.channelType` | string |  |
| `channel.description` | string |  |
| `channel.id` | string |  |
| `channel.isArchived` | boolean |  |
| `channel.isHidden` | boolean |  |
| `channel.isMain` | boolean |  |
| `channel.isMember` | boolean |  |
| `channel.lastMessageTimestamp` | string |  |
| `channel.name` | string |  |
| `channel.timestamp` | string |  |
| `channel.workspaceId` | string |  |
| `users` | array<string> |  |

## Native endpoint

Through the native Pumble API, this operation is `GET /getChannel` (base URL `https://pumble-api-keys.addons.marketplace.cake.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-channel.md) for the provider-specific parameters and requirements.

