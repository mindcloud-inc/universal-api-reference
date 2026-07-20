# Level: Remove Devices from Group

Removes devices from a group in Level.

```
DELETE https://connect.mindcloud.co/v1/universal/level/latest/actions/remove-devices-from-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Level `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/level/latest/actions/remove-devices-from-group?connectionId=$CONNECTION_ID&deviceIds%5B%5D=string&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "deviceIds[]": "string",
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/level/latest/actions/remove-devices-from-group?${params}`, {
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
| `deviceIds[]` | array<string> | yes | An array of device IDs to remove from the group. Accepts multiple values as an array. |
| `id` | string | yes | ID of the group. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |

## Native endpoint

Through the native Level API, this operation is `DELETE /groups/{id}/devices` (base URL `https://api.level.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-devices-from-group.md) for the provider-specific parameters and requirements.

