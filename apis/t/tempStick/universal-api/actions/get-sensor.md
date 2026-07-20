# Temp Stick: Get Sensor

Retrieves settings for a specific Temp Stick sensor.

```
GET https://connect.mindcloud.co/v1/universal/tempStick/latest/actions/get-sensor
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Temp Stick `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tempStick/latest/actions/get-sensor?connectionId=$CONNECTION_ID&sensorId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sensorId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tempStick/latest/actions/get-sensor?${params}`, {
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
| `sensorId` | string | yes | The ID of the sensor you want to get readings from |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Temp Stick API returns.

## Native endpoint

Through the native Temp Stick API, this operation is `GET /sensor/:sensor_id` (base URL `https://tempstickapi.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sensor.md) for the provider-specific parameters and requirements.

