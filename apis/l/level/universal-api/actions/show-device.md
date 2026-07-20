# Level: Show Device

Retrieves an existing device from Level.

```
GET https://connect.mindcloud.co/v1/universal/level/latest/actions/show-device
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Level `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/level/latest/actions/show-device?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/level/latest/actions/show-device?${params}`, {
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
| `id` | string | yes | The ID of the device to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "groupId": "string",
      "hostname": "Ava Chen",
      "id": "string",
      "nickname": "Ava Chen",
      "online": true,
      "platform": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `groupId` | string |  |
| `hostname` | string |  |
| `id` | string |  |
| `nickname` | string |  |
| `online` | boolean |  |
| `platform` | string |  |

## Native endpoint

Through the native Level API, this operation is `GET /devices/{id}` (base URL `https://api.level.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/show-device.md) for the provider-specific parameters and requirements.

