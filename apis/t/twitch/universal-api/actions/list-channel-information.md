# Twitch: List Channel Information

Retrieves broadcaster channel information from Twitch.

```
GET https://connect.mindcloud.co/v1/universal/twitch/latest/actions/list-channel-information
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Twitch `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/twitch/latest/actions/list-channel-information?connectionId=$CONNECTION_ID&broadcasterId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "broadcasterId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/twitch/latest/actions/list-channel-information?${params}`, {
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
| `broadcasterId` | string | yes | The ID of the broadcaster whose channel you want to get. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "broadcasterId": "string",
      "broadcasterLanguage": "string",
      "broadcasterLogin": "string",
      "broadcasterName": "Ava Chen",
      "delay": 1,
      "gameId": "string",
      "gameName": "Ava Chen",
      "isBrandedContent": true,
      "tags": [
        "string"
      ],
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `broadcasterId` | string |  |
| `broadcasterLanguage` | string |  |
| `broadcasterLogin` | string |  |
| `broadcasterName` | string |  |
| `delay` | number |  |
| `gameId` | string |  |
| `gameName` | string |  |
| `isBrandedContent` | boolean |  |
| `tags[]` | string |  |
| `title` | string |  |

## Native endpoint

Through the native Twitch API, this operation is `GET /channels` (base URL `https://api.twitch.tv/helix`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-channel-information.md) for the provider-specific parameters and requirements.

