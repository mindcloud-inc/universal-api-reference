# Level Universal API Examples

These examples use the MindCloud API key and Level connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Groups

Retrieves a list of groups from Level.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/level/latest/actions/list-groups?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/level/latest/actions/list-groups?${params}`, {
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
      "data": [
        {
          "childIds": [
            "string"
          ],
          "descendentDeviceCount": 1,
          "deviceCount": 1,
          "id": "string",
          "name": "Ava Chen",
          "parentId": "string"
        }
      ],
      "hasMore": true
    }
  ],
  "meta": {}
}
```

See the full [List Groups action reference](actions/list-groups.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/level/latest/actions/list-groups).

## Assign Devices to Group

Assigns devices to a group in Level.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/level/latest/actions/assign-devices-to-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "deviceIds[]": [
    "string"
  ],
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/level/latest/actions/assign-devices-to-group', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "deviceIds[]": ["string"],
    "id": "string"
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
      "group": {
        "childIds": [
          "string"
        ],
        "descendentDeviceCount": 1,
        "deviceCount": 1,
        "id": "string",
        "name": "Ava Chen",
        "parentId": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [Assign Devices to Group action reference](actions/assign-devices-to-group.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/level/latest/actions/assign-devices-to-group).
