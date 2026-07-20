# timeBuzzer: Create Tile



```
POST https://connect.mindcloud.co/v1/universal/timeBuzzer/latest/actions/create-tile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a timeBuzzer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/timeBuzzer/latest/actions/create-tile" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "type": "string",
  "layer": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/timeBuzzer/latest/actions/create-tile', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "type": "string",
    "layer": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Tile name. |
| `parents[]` | array<number> | no | Optional parent tile IDs. |
| `archived` | boolean | no | Whether the tile is archived. |
| `type` | string | yes | Tile type. |
| `layer` | number | yes | Layer ID for the tile. |
| `favorite` | boolean | no | Whether the tile is a favorite. |
| `color` | string | no | ARGB color hex for the tile. |
| `description` | string | no | Optional tile description. |
| `customData` | string | no | Optional custom data string. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "assignedGroups": [
        {}
      ],
      "assignedUsers": [
        {}
      ],
      "children": [
        1
      ],
      "color": "string",
      "customData": "string",
      "description": "string",
      "favorite": true,
      "id": 1,
      "isAvailableToAllUsers": true,
      "layer": 1,
      "name": "Ava Chen",
      "parents": [
        1
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean | Whether the tile is archived. |
| `assignedGroups` | array<object> | Assigned group records. |
| `assignedUsers` | array<object> | Assigned user records. |
| `children` | array<number> | Child tile IDs. |
| `color` | string | Tile color. |
| `customData` | string | Custom tile data when present. |
| `description` | string | Tile description. |
| `favorite` | boolean | Whether the tile is a favorite. |
| `id` | number | Tile ID. |
| `isAvailableToAllUsers` | boolean | Whether the tile is available to all users. |
| `layer` | number | Layer ID. |
| `name` | string | Tile name. |
| `parents` | array<number> | Parent tile IDs. |
| `type` | string | Tile type. |

## Native endpoint

Through the native timeBuzzer API, this operation is `POST /open-api/tiles` (base URL `https://my.timebuzzer.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-tile.md) for the provider-specific parameters and requirements.

