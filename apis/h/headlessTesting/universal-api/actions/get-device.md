# Headless Testing: Get Device

Retrieves a device from Headless Testing.

```
GET https://connect.mindcloud.co/v1/universal/headlessTesting/latest/actions/get-device
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Headless Testing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/headlessTesting/latest/actions/get-device?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/headlessTesting/latest/actions/get-device?${params}`, {
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
| `id` | string | yes | Device identifier from the path. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deviceName": "Ava Chen",
      "id": 1,
      "platformName": "Ava Chen",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deviceName` | string |  |
| `id` | number |  |
| `platformName` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Headless Testing API, this operation is `GET /devices/:id` (base URL `https://api.testingbot.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-device.md) for the provider-specific parameters and requirements.

