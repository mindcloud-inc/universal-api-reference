# ClassDo Universal API Examples

These examples use the MindCloud API key and ClassDo connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Rooms

Retrieves a list of rooms from ClassDo.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/classDo/latest/actions/list-rooms?connectionId=$CONNECTION_ID&query=query%20ListRooms%20%7B%20viewer%20%7B%20rooms(input%3A%20%7B%20first%3A%2020%2C%20orderBy%3A%20createdAt_DESC%20%7D)%20%7B%20edges%20%7B%20node%20%7B%20id%20name%20%7D%20%7D%20%7D%20%7D%20%7D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "query ListRooms { viewer { rooms(input: { first: 20, orderBy: createdAt_DESC }) { edges { node { id name } } } } }"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/classDo/latest/actions/list-rooms?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "viewer": {
          "rooms": {
            "edges": [
              {
                "node": {
                  "id": "string",
                  "name": "Ava Chen"
                }
              }
            ]
          }
        }
      },
      "errors": [
        {
          "message": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Rooms action reference](actions/list-rooms.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/classDo/latest/actions/list-rooms).

## Add Room Members

Adds members to a room in ClassDo.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/classDo/latest/actions/add-room-members" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "query": "mutation AddRoomMembers { addRoomMembers(data: { roomId: \"ROOM_ID\", userIds: [\"USER_ID\"] }) { id } }"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/classDo/latest/actions/add-room-members', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "query": "mutation AddRoomMembers { addRoomMembers(data: { roomId: \"ROOM_ID\", userIds: [\"USER_ID\"] }) { id } }"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "addRoomMembers": {
          "id": "string"
        }
      },
      "errors": [
        {
          "message": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [Add Room Members action reference](actions/add-room-members.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/classDo/latest/actions/add-room-members).
