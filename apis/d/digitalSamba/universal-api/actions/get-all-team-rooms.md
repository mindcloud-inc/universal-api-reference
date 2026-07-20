# Digital Samba: Get all team rooms

Retrieves team rooms from Digital Samba.

```
GET https://connect.mindcloud.co/v1/universal/digitalSamba/latest/actions/get-all-team-rooms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Digital Samba `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/digitalSamba/latest/actions/get-all-team-rooms?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/digitalSamba/latest/actions/get-all-team-rooms?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `after` | string | no | The UUID of the room or room friendly URL after which records will be returned. |
| `tag` | string | no | string\|array Filter rooms by tags. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "audioOnJoinEnabled": true,
      "audioQuality": "string",
      "autoPipEnabled": true,
      "backgroundColor": "string",
      "description": "string",
      "friendlyUrl": "https://example.com",
      "hdVideoQuality": "string",
      "id": "string",
      "language": "string",
      "languages": [
        "string"
      ],
      "languageSelectionEnabled": true,
      "maxBroadcasters": 1,
      "maxParticipants": 1,
      "paletteMode": "string",
      "pipEnabled": true,
      "primaryColor": "string",
      "privacy": "string",
      "roomReactionsEnabled": true,
      "toolbarColor": "string",
      "toolbarEnabled": true,
      "toolbarPosition": "string",
      "topbarEnabled": true,
      "topic": "string",
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
| `audioQuality` | string |  |
| `autoPipEnabled` | boolean |  |
| `backgroundColor` | string |  |
| `description` | string |  |
| `friendlyUrl` | string |  |
| `hdVideoQuality` | string |  |
| `id` | string |  |
| `language` | string |  |
| `languages` | array<string> |  |
| `languageSelectionEnabled` | boolean |  |
| `maxBroadcasters` | number |  |
| `maxParticipants` | number |  |
| `paletteMode` | string |  |
| `pipEnabled` | boolean |  |
| `primaryColor` | string |  |
| `privacy` | string |  |
| `roomReactionsEnabled` | boolean |  |
| `toolbarColor` | string |  |
| `toolbarEnabled` | boolean |  |
| `toolbarPosition` | string |  |
| `topbarEnabled` | boolean |  |
| `topic` | string |  |
| `videoOnJoinEnabled` | boolean |  |

## Native endpoint

Through the native Digital Samba API, this operation is `GET /rooms` (base URL `https://api.digitalsamba.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-all-team-rooms.md) for the provider-specific parameters and requirements.

