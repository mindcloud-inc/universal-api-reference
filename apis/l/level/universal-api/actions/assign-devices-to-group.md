# Level: Assign Devices to Group

Assigns devices to a group in Level.

```
PUT https://connect.mindcloud.co/v1/universal/level/latest/actions/assign-devices-to-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Level `connectionId` ([setup](../authentication.md)).

## Example request

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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `deviceIds[]` | array<string> | yes | An array of device IDs to assign to the group. Accepts multiple values as an array. |
| `id` | string | yes | ID of the group. |

## Response

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

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `group.childIds` | array<string> |  |
| `group.descendentDeviceCount` | number |  |
| `group.deviceCount` | number |  |
| `group.id` | string |  |
| `group.name` | string |  |
| `group.parentId` | string |  |

## Native endpoint

Through the native Level API, this operation is `POST /groups/{id}/devices` (base URL `https://api.level.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/assign-devices-to-group.md) for the provider-specific parameters and requirements.

