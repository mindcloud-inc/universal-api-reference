# Digital Samba: Get the specified room

Retrieves a room from Digital Samba.

```
GET https://connect.mindcloud.co/v1/universal/digitalSamba/latest/actions/get-the-specified-room
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Digital Samba `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/digitalSamba/latest/actions/get-the-specified-room?connectionId=$CONNECTION_ID&room=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "room": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/digitalSamba/latest/actions/get-the-specified-room?${params}`, {
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
| `room` | string | yes | Room path parameter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "audioOnJoinEnabled": true,
      "backgroundColor": "string",
      "customLogo": "string",
      "description": "string",
      "friendlyUrl": "https://example.com",
      "id": "string",
      "isLocked": true,
      "language": "string",
      "languageSelectionEnabled": true,
      "logoEnabled": true,
      "maxBroadcasters": 1,
      "maxParticipants": 1,
      "paletteMode": "string",
      "participantsListEnabled": true,
      "primaryColor": "string",
      "privacy": "string",
      "recordingLogoEnabled": true,
      "recordingsEnabled": true,
      "screenshareEnabled": true,
      "toolbarColor": "string",
      "toolbarEnabled": true,
      "toolbarPosition": "string",
      "topbarEnabled": true,
      "videoOnJoinEnabled": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `audioOnJoinEnabled` | boolean |  |
| `backgroundColor` | string |  |
| `customLogo` | string |  |
| `description` | string |  |
| `friendlyUrl` | string |  |
| `id` | string |  |
| `isLocked` | boolean |  |
| `language` | string |  |
| `languageSelectionEnabled` | boolean |  |
| `logoEnabled` | boolean |  |
| `maxBroadcasters` | number |  |
| `maxParticipants` | number |  |
| `paletteMode` | string |  |
| `participantsListEnabled` | boolean |  |
| `primaryColor` | string |  |
| `privacy` | string |  |
| `recordingLogoEnabled` | boolean |  |
| `recordingsEnabled` | boolean |  |
| `screenshareEnabled` | boolean |  |
| `toolbarColor` | string |  |
| `toolbarEnabled` | boolean |  |
| `toolbarPosition` | string |  |
| `topbarEnabled` | boolean |  |
| `videoOnJoinEnabled` | boolean |  |

## Native endpoint

Through the native Digital Samba API, this operation is `GET /rooms/:room` (base URL `https://api.digitalsamba.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-the-specified-room.md) for the provider-specific parameters and requirements.

