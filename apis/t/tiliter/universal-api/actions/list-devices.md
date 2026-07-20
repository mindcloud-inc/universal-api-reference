# Tiliter: List Devices

Retrieves devices from the Tiliter Recognition API.

```
GET https://connect.mindcloud.co/v1/universal/tiliter/latest/actions/list-devices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tiliter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tiliter/latest/actions/list-devices?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tiliter/latest/actions/list-devices?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "devices": [
        {
          "cameras": [
            "string"
          ],
          "departments": [
            "string"
          ],
          "deviceId": "string",
          "operationalMode": "string",
          "storeId": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `devices` | array<object> |  |
| `devices[].cameras` | array<string> |  |
| `devices[].cameras[]` | string |  |
| `devices[].departments` | array<string> |  |
| `devices[].departments[]` | string |  |
| `devices[].deviceId` | string |  |
| `devices[].operationalMode` | string |  |
| `devices[].storeId` | string |  |

## Native endpoint

Through the native Tiliter API, this operation is `GET /devices/` (base URL `https://recognition.services.tiliter.com/v1/15`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-devices.md) for the provider-specific parameters and requirements.

