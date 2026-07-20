# Pushbullet: Delete Device

Deletes an existing device from Pushbullet.

```
DELETE https://connect.mindcloud.co/v1/universal/pushBullet/latest/actions/delete-device
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pushbullet `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/pushBullet/latest/actions/delete-device?connectionId=$CONNECTION_ID&device_iden=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "device_iden": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pushBullet/latest/actions/delete-device?${params}`, {
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
| `device_iden` | string | yes | Device identifier to delete. |

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

Through the native Pushbullet API, this operation is `DELETE /devices/:device_iden` (base URL `https://api.pushbullet.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-device.md) for the provider-specific parameters and requirements.

