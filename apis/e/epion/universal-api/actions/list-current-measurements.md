# Epion: List Current Measurements

Retrieves current device measurements from Epion.

```
GET https://connect.mindcloud.co/v1/universal/epion/latest/actions/list-current-measurements
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Epion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/epion/latest/actions/list-current-measurements?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/epion/latest/actions/list-current-measurements?${params}`, {
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
      "co2": 1,
      "deviceId": "string",
      "deviceName": "Ava Chen",
      "fwVersion": "string",
      "humidity": 1,
      "pressure": 1,
      "temperature": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `co2` | number | Current CO2 concentration in parts per million. |
| `deviceId` | string | Unique Epion device identifier. |
| `deviceName` | string | Display name of the Epion device. |
| `fwVersion` | string | Firmware version reported by the device. |
| `humidity` | number | Current relative humidity percentage. |
| `pressure` | number | Current atmospheric pressure in hectopascals. |
| `temperature` | number | Current temperature in degrees Celsius. |

## Native endpoint

Through the native Epion API, this operation is `GET /api/current` (base URL `https://api.epion.nl`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-current-measurements.md) for the provider-specific parameters and requirements.

