# Twitch: Modify Channel Information

Updates broadcaster channel information in Twitch.

```
PUT https://connect.mindcloud.co/v1/universal/twitch/latest/actions/modify-channel-information
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Twitch `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/twitch/latest/actions/modify-channel-information" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "broadcasterId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/twitch/latest/actions/modify-channel-information', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "broadcasterId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `broadcasterId` | string | yes | The broadcaster whose channel to update. This ID must match the user ID in the access token. |
| `gameId` | string | no | Updates the active game/category. Use 0 or an empty string to unset the game. |
| `broadcasterLanguage` | string | no | ISO 639-1 language code for the stream, or other when Twitch does not support the language. |
| `title` | string | no | Updates the stream title. Twitch does not allow an empty title. |
| `delay` | string | no | Broadcast delay in seconds. Only Partner channels may set this value. Maximum 900. |
| `tags` | string | no | Channel-defined tags to apply. Maximum 10 tags; each tag is limited to 25 characters and may not contain spaces or special characters. |
| `contentClassificationLabels[].id` | string | no | Content Classification Label to enable or disable on the channel. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | string | Empty response body returned when the channel information is updated successfully. |

## Native endpoint

Through the native Twitch API, this operation is `PATCH /channels` (base URL `https://api.twitch.tv/helix`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/modify-channel-information.md) for the provider-specific parameters and requirements.

