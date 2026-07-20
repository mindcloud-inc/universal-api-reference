# Screenly: List Playlists

Retrieves playlists from Screenly.

```
GET https://connect.mindcloud.co/v1/universal/screenly/latest/actions/list-playlists
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Screenly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/screenly/latest/actions/list-playlists?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/screenly/latest/actions/list-playlists?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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

Through the native Screenly API, this operation is `GET /playlists/` (base URL `https://api.screenlyapp.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-playlists.md) for the provider-specific parameters and requirements.

