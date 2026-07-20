# Carbon Intensity: Get Carbon Intensity Statistics

Retrieves carbon intensity statistics between two specified datetimes.

```
GET https://connect.mindcloud.co/v1/universal/carbonIntensity/latest/actions/get-carbon-intensity-statistics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Carbon Intensity `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/carbonIntensity/latest/actions/get-carbon-intensity-statistics?connectionId=$CONNECTION_ID&from=2026-04-12T12%3A00Z&to=2026-04-12T12%3A00Z" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "from": "2026-04-12T12:00Z",
  "to": "2026-04-12T12:00Z"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/carbonIntensity/latest/actions/get-carbon-intensity-statistics?${params}`, {
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
| `to` | string | yes | Datetime in ISO-8601 format YYYY-MM-DDThh:mmZ exactly as required by the API path. Example: `2026-04-12T12:00Z`. |

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
            "average": 1,
            "index": "string",
            "max": 1,
            "min": 1
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
| `data[].intensity.average` | number |  |
| `data[].intensity.index` | string |  |
| `data[].intensity.max` | number |  |
| `data[].intensity.min` | number |  |
| `data[].to` | string |  |

## Native endpoint

Through the native Carbon Intensity API, this operation is `GET /intensity/stats/:from/:to` (base URL `https://api.carbonintensity.org.uk`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-carbon-intensity-statistics.md) for the provider-specific parameters and requirements.

