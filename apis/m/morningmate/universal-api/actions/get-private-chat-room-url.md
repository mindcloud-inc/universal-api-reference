# Morningmate: Get Private Chat Room URL

Retrieves a private chat room URL from Morningmate.

```
GET https://connect.mindcloud.co/v1/universal/morningmate/latest/actions/get-private-chat-room-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Morningmate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/morningmate/latest/actions/get-private-chat-room-url?connectionId=$CONNECTION_ID&registerId=apps%40mindcloud.co&receiverId=colleague%40company.name" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "registerId": "apps@mindcloud.co",
  "receiverId": "colleague@company.name"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/morningmate/latest/actions/get-private-chat-room-url?${params}`, {
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
| `registerId` | string | yes | Morningmate author user ID Example: `apps@mindcloud.co`. |
| `receiverId` | string | yes | Morningmate receiver user ID Example: `colleague@company.name`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "launcherUrl": "https://example.com",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `launcherUrl` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Morningmate API, this operation is `GET /v1/chats/urls` (base URL `https://api.morningmate.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-private-chat-room-url.md) for the provider-specific parameters and requirements.

