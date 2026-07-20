# Viewneo: List Playlists

Retrieves playlists for the current account in Viewneo.

```
GET https://connect.mindcloud.co/v1/universal/viewneo/latest/actions/list-playlists
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Viewneo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/viewneo/latest/actions/list-playlists?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/viewneo/latest/actions/list-playlists?${params}`, {
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
      "comment": "string",
      "companyId": 1,
      "createdAt": "string",
      "deletedAt": {},
      "eventsCount": 1,
      "id": 1,
      "isAdvertised": 1,
      "isDefault": 1,
      "isDemo": 1,
      "isShared": 1,
      "label": {},
      "name": "Ava Chen",
      "numberOfEntries": 1,
      "playbackEntryCount": 1,
      "playbackOrder": 1,
      "playbackRule": 1,
      "type": 1,
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comment` | string |  |
| `companyId` | number |  |
| `createdAt` | string |  |
| `deletedAt` | object |  |
| `eventsCount` | number |  |
| `id` | number |  |
| `isAdvertised` | number |  |
| `isDefault` | number |  |
| `isDemo` | number |  |
| `isShared` | number |  |
| `label` | object |  |
| `name` | string |  |
| `numberOfEntries` | number |  |
| `playbackEntryCount` | number |  |
| `playbackOrder` | number |  |
| `playbackRule` | number |  |
| `type` | number |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Viewneo API, this operation is `GET /playlist` (base URL `https://cloud.viewneo.com/api/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-playlists.md) for the provider-specific parameters and requirements.

