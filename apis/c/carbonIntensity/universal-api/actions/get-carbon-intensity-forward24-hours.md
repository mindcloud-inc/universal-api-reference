# Carbon Intensity: Get Carbon Intensity Forward 24 Hours

Retrieves carbon intensity for 24 hours after a datetime.

```
GET https://connect.mindcloud.co/v1/universal/carbonIntensity/latest/actions/get-carbon-intensity-forward24-hours
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Carbon Intensity `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/carbonIntensity/latest/actions/get-carbon-intensity-forward24-hours?connectionId=$CONNECTION_ID&from=2026-04-12T12%3A00Z" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "from": "2026-04-12T12:00Z"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/carbonIntensity/latest/actions/get-carbon-intensity-forward24-hours?${params}`, {
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
| `from` | string | yes | Datetime in ISO-8601 format YYYY-MM-DDThh:mmZ exactly as required by the API path. Example: `2026-04-12T12:00Z`. |

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

Through the native Carbon Intensity API, this operation is `GET /intensity/:from/fw24h` (base URL `https://api.carbonintensity.org.uk`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-carbon-intensity-forward24-hours.md) for the provider-specific parameters and requirements.

