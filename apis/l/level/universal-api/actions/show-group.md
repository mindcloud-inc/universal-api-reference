# Level: Show Group

Retrieves an existing group from Level.

```
GET https://connect.mindcloud.co/v1/universal/level/latest/actions/show-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Level `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/level/latest/actions/show-group?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/level/latest/actions/show-group?${params}`, {
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
| `id` | string | yes | The ID of the group to retrieve. |

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

Through the native Level API, this operation is `GET /groups/{id}` (base URL `https://api.level.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/show-group.md) for the provider-specific parameters and requirements.

