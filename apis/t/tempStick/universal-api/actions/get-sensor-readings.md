# Temp Stick: Get Sensor Readings

Retrieves readings for a Temp Stick sensor over a selected period.

```
GET https://connect.mindcloud.co/v1/universal/tempStick/latest/actions/get-sensor-readings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Temp Stick `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tempStick/latest/actions/get-sensor-readings?connectionId=$CONNECTION_ID&offset=0&sensorId=string&setting=today" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "offset": "0",
  "sensorId": "string",
  "setting": "today"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tempStick/latest/actions/get-sensor-readings?${params}`, {
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
| `end` | string | no | The end date in YYYY-MM-DD format if custom is selected |
| `offset` | number | yes | Timezone offset in seconds from UTC used to calculate the specified time period Default: `0`. |
| `sensorId` | string | yes | The ID of the sensor you want to get readings from |
| `setting` | string | yes | The time period you want to grab readings from Default: `today`. |
| `start` | string | no | The start date in YYYY-MM-DD format if custom is selected |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Temp Stick API returns.

## Native endpoint

Through the native Temp Stick API, this operation is `GET /sensor/:sensor_id/readings` (base URL `https://tempstickapi.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sensor-readings.md) for the provider-specific parameters and requirements.

