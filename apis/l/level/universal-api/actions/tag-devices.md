# Level: Tag Devices

Applies a tag to devices in Level.

```
PUT https://connect.mindcloud.co/v1/universal/level/latest/actions/tag-devices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Level `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/level/latest/actions/tag-devices" \
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
const response = await fetch('https://connect.mindcloud.co/v1/universal/level/latest/actions/tag-devices', {
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
| `deviceIds[]` | array<string> | yes | An array of device IDs to tag. Accepts multiple values as an array. |
| `id` | string | yes | ID of the tag to apply. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deviceCount": 1,
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deviceCount` | number |  |
| `id` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Level API, this operation is `POST /tags/{id}/devices` (base URL `https://api.level.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/tag-devices.md) for the provider-specific parameters and requirements.

