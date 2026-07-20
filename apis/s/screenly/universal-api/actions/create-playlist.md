# Screenly: Create Playlist

Creates a new playlist in Screenly.

```
POST https://connect.mindcloud.co/v1/universal/screenly/latest/actions/create-playlist
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Screenly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/screenly/latest/actions/create-playlist" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/screenly/latest/actions/create-playlist', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `isEnabled` | boolean | no |  |
| `predicate` | string | no |  |
| `priority` | number | no |  |
| `title` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assets": [
        {
          "duration": 1,
          "id": "string"
        }
      ],
      "duration": 1,
      "groups": [
        {
          "id": "string",
          "name": "Ava Chen",
          "url": "https://example.com"
        }
      ],
      "id": "string",
      "isEnabled": true,
      "predicate": "string",
      "priority": 1,
      "title": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assets[].duration` | number |  |
| `assets[].id` | string |  |
| `duration` | number |  |
| `groups[].id` | string |  |
| `groups[].name` | string |  |
| `groups[].url` | string |  |
| `id` | string |  |
| `isEnabled` | boolean |  |
| `predicate` | string |  |
| `priority` | number |  |
| `title` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Screenly API, this operation is `POST /playlists/` (base URL `https://api.screenlyapp.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-playlist.md) for the provider-specific parameters and requirements.

