# LightwaveRF Power: Read Historical Data

Retrieves historical data from LightwaveRF Power.

```
GET https://connect.mindcloud.co/v1/universal/lightwaveRFPower/latest/actions/read-historical-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LightwaveRF Power `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lightwaveRFPower/latest/actions/read-historical-data?connectionId=$CONNECTION_ID&deviceId=string&featureId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "deviceId": "string",
  "featureId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lightwaveRFPower/latest/actions/read-historical-data?${params}`, {
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
| `deviceId` | string | yes | The LightwaveRF device identifier whose historical data should be read. |
| `featureId` | string | yes | The LightwaveRF feature identifier whose historical data should be read. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `start` | number | no | The earliest timestamp in milliseconds to include in the historical data query. |
| `end` | number | no | The latest timestamp in milliseconds to include in the historical data query. |
| `limit` | number | no | The maximum number of historical records to return. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deviceId": "string",
      "featureId": "string",
      "timestamp": 1,
      "value": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deviceId` | string |  |
| `featureId` | string |  |
| `timestamp` | number |  |
| `value` | number |  |

## Native endpoint

Through the native LightwaveRF Power API, this operation is `GET /v1/data/{deviceId}/{featureId}` (base URL `https://publicapi.lightwaverf.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/read-historical-data.md) for the provider-specific parameters and requirements.

