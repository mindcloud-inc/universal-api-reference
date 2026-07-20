# LightwaveRF Heating: Read Heating Historical Data

Retrieves historical heating data from LightwaveRF Heating.

```
GET https://connect.mindcloud.co/v1/universal/lightwaveRFHeating/latest/actions/read-heating-historical-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LightwaveRF Heating `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lightwaveRFHeating/latest/actions/read-heating-historical-data?connectionId=$CONNECTION_ID&deviceId=string&featureId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "deviceId": "string",
  "featureId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lightwaveRFHeating/latest/actions/read-heating-historical-data?${params}`, {
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
| `deviceId` | string | yes | The LightwaveRF heating device identifier whose historical data should be read. |
| `featureId` | string | yes | The LightwaveRF heating feature identifier whose historical data should be read. |

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
      "data": [
        {}
      ],
      "deviceId": "string",
      "featureId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | Historical heating data points. |
| `deviceId` | string | Device identifier. |
| `featureId` | string | Feature identifier. |

## Native endpoint

Through the native LightwaveRF Heating API, this operation is `GET /v1/data/{deviceId}/{featureId}` (base URL `https://publicapi.lightwaverf.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/read-heating-historical-data.md) for the provider-specific parameters and requirements.

