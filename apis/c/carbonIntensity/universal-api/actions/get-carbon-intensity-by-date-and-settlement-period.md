# Carbon Intensity: Get Carbon Intensity By Date and Settlement Period

Retrieves carbon intensity for a date and settlement period.

```
GET https://connect.mindcloud.co/v1/universal/carbonIntensity/latest/actions/get-carbon-intensity-by-date-and-settlement-period
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Carbon Intensity `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/carbonIntensity/latest/actions/get-carbon-intensity-by-date-and-settlement-period?connectionId=$CONNECTION_ID&date=2026-04-12&period=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "date": "2026-04-12",
  "period": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/carbonIntensity/latest/actions/get-carbon-intensity-by-date-and-settlement-period?${params}`, {
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
| `date` | string | yes | Date in YYYY-MM-DD format exactly as required by the API path. Example: `2026-04-12`. |
| `period` | number | yes | Settlement period number for the selected date. Example: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "from": "string",
          "intensity": {
            "actual": 1,
            "forecast": 1,
            "index": "string"
          },
          "to": "string"
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
| `data` | array<object> |  |
| `data[].from` | string |  |
| `data[].intensity` | object |  |
| `data[].intensity.actual` | number |  |
| `data[].intensity.forecast` | number |  |
| `data[].intensity.index` | string |  |
| `data[].to` | string |  |

## Native endpoint

Through the native Carbon Intensity API, this operation is `GET /intensity/date/:date/:period` (base URL `https://api.carbonintensity.org.uk`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-carbon-intensity-by-date-and-settlement-period.md) for the provider-specific parameters and requirements.

