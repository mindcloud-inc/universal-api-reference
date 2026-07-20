# Golemio API: List Air Quality Station History

Finds air quality station history in the Golemio API.

```
GET https://connect.mindcloud.co/v1/universal/golemioAPI/latest/actions/list-air-quality-station-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Golemio API `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/golemioAPI/latest/actions/list-air-quality-station-history?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/golemioAPI/latest/actions/list-air-quality-station-history?${params}`, {
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
      "id": "string",
      "measurement": {
        "AQHourlyIndex": "https://example.com",
        "components": {
          "averagedTime": {
            "averagedHours": "string",
            "value": 1
          },
          "type": "string"
        }
      },
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Air-quality station identifier. |
| `measurement` | object | Air-quality measurement payload. |
| `measurement.AQHourlyIndex` | string | Hourly air-quality index. |
| `measurement.components` | array<object> | Measured pollutant components. |
| `measurement.components.averagedTime` | object | Averaging window and value. |
| `measurement.components.averagedTime.averagedHours` | string | Averaging window in hours. |
| `measurement.components.averagedTime.value` | number | Measured averaged value. |
| `measurement.components.type` | string | Component pollutant type. |
| `updatedAt` | date | Measurement update time when returned by Golemio. |

## Native endpoint

Through the native Golemio API API, this operation is `GET /v2/airqualitystations/history` (base URL `https://api.golemio.cz`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-air-quality-station-history.md) for the provider-specific parameters and requirements.

