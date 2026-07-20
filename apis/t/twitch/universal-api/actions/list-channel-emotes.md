# Twitch: List Channel Emotes

Retrieves channel emote records from Twitch.

```
GET https://connect.mindcloud.co/v1/universal/twitch/latest/actions/list-channel-emotes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Twitch `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/twitch/latest/actions/list-channel-emotes?connectionId=$CONNECTION_ID&broadcasterId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "broadcasterId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/twitch/latest/actions/list-channel-emotes?${params}`, {
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
| `broadcasterId` | string | yes | An ID that identifies the broadcaster whose emotes you want to get. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "emoteSetId": "string",
      "emoteType": "string",
      "format": [
        "string"
      ],
      "id": "string",
      "name": "Ava Chen",
      "scale": [
        "string"
      ],
      "themeMode": [
        "string"
      ],
      "tier": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `emoteSetId` | string |  |
| `emoteType` | string |  |
| `format[]` | string |  |
| `id` | string |  |
| `name` | string |  |
| `scale[]` | string |  |
| `themeMode[]` | string |  |
| `tier` | string |  |

## Native endpoint

Through the native Twitch API, this operation is `GET /chat/emotes` (base URL `https://api.twitch.tv/helix`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-channel-emotes.md) for the provider-specific parameters and requirements.

