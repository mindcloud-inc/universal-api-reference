# GSA Site Scanning: Get Scan Device

Retrieves a scan device by device ID.

```
GET https://connect.mindcloud.co/v1/universal/gSASiteScanning/latest/actions/get-scan-device
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GSA Site Scanning `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gSASiteScanning/latest/actions/get-scan-device?connectionId=$CONNECTION_ID&deviceId=scanner-123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "deviceId": "scanner-123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gSASiteScanning/latest/actions/get-scan-device?${params}`, {
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
| `deviceId` | string | yes | Device identifier. Example: `scanner-123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deviceId": "string",
      "deviceInUse": true,
      "deviceStatus": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deviceId` | string | The identifier of the device. |
| `deviceInUse` | boolean | Whether the device is in use. |
| `deviceStatus` | string | The status of the device. |

## Native endpoint

Through the native GSA Site Scanning API, this operation is `GET /scan/v2/device/:deviceId` (base URL `https://api.sitaflex.aero`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-scan-device.md) for the provider-specific parameters and requirements.

