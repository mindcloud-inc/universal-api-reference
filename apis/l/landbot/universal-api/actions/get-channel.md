# Landbot: Get Channel

Retrieves a channel from Landbot.

```
GET https://connect.mindcloud.co/v1/universal/landbot/latest/actions/get-channel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Landbot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/landbot/latest/actions/get-channel?connectionId=$CONNECTION_ID&channelId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "channelId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/landbot/latest/actions/get-channel?${params}`, {
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
| `channelId` | number | yes | Channel ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "chats": 1,
      "createdAt": 1,
      "hooks": [
        "string"
      ],
      "hsm": 1,
      "id": 1,
      "name": "Ava Chen",
      "token": "string",
      "type": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `chats` | number |  |
| `createdAt` | number |  |
| `hooks[]` | string |  |
| `hsm` | number |  |
| `id` | number |  |
| `name` | string |  |
| `token` | string |  |
| `type` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native Landbot API, this operation is `GET /v1/channels/:channel_id/` (base URL `https://api.landbot.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-channel.md) for the provider-specific parameters and requirements.

