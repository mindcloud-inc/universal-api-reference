# Level: Update Group

Updates an existing group in Level.

```
PUT https://connect.mindcloud.co/v1/universal/level/latest/actions/update-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Level `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/level/latest/actions/update-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/level/latest/actions/update-group', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The ID of the group to update. |

## Response

```json
{
  "success": true,
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
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `childIds` | array<string> |  |
| `descendentDeviceCount` | number |  |
| `deviceCount` | number |  |
| `id` | string |  |
| `name` | string |  |
| `parentId` | string |  |

## Native endpoint

Through the native Level API, this operation is `PATCH /groups/{id}` (base URL `https://api.level.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-group.md) for the provider-specific parameters and requirements.

