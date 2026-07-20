# timeBuzzer: Update Tile



```
PUT https://connect.mindcloud.co/v1/universal/timeBuzzer/latest/actions/update-tile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a timeBuzzer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/timeBuzzer/latest/actions/update-tile" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "name": "Ava Chen",
  "type": "string",
  "layer": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/timeBuzzer/latest/actions/update-tile', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
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
| `id` | number | yes | The tile ID. |
| `name` | string | yes | The tile name. |
| `parents[]` | array<number> | no | The parent tile IDs. Accepts multiple values as an array. |
| `archived` | boolean | no | Whether the tile is archived. |
| `type` | string | yes | The tile type. |
| `layer` | number | yes | The layer ID. |
| `favorite` | boolean | no | Whether the tile is a favorite. |
| `color` | string | no | The tile color. |
| `description` | string | no | The tile description. |
| `customData` | string | no | Custom tile data. |

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

Through the native timeBuzzer API, this operation is `PUT /open-api/tiles/:id` (base URL `https://my.timebuzzer.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-tile.md) for the provider-specific parameters and requirements.

