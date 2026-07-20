# Viewneo: Get Playlist

Retrieves a specific playlist from Viewneo.

```
GET https://connect.mindcloud.co/v1/universal/viewneo/latest/actions/get-playlist
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Viewneo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/viewneo/latest/actions/get-playlist?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/viewneo/latest/actions/get-playlist?${params}`, {
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
| `id` | number | yes |  |

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

Through the native Viewneo API, this operation is `GET /playlist/:id` (base URL `https://cloud.viewneo.com/api/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-playlist.md) for the provider-specific parameters and requirements.

