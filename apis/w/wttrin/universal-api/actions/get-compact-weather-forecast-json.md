# wttr.in: Get Compact Weather Forecast JSON

Retrieves compact weather forecast JSON from wttr.in.

```
GET https://connect.mindcloud.co/v1/universal/wttrin/latest/actions/get-compact-weather-forecast-json
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a wttr.in `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wttrin/latest/actions/get-compact-weather-forecast-json?connectionId=$CONNECTION_ID&location=London" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "location": "London"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wttrin/latest/actions/get-compact-weather-forecast-json?${params}`, {
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
| `location` | string | yes | City, airport code, domain, postal code, GPS coordinates, or supported wttr.in location expression. Example: `London`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "current_condition": [
        {}
      ],
      "nearest_area": [
        {}
      ],
      "request": [
        {}
      ],
      "weather": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `current_condition` | array<object> | Current observed weather conditions. |
| `nearest_area` | array<object> | Resolved nearest weather area for the request. |
| `request` | array<object> | Location request metadata. |
| `weather` | array<object> | Compact forecast days without hourly data. |

## Native endpoint

Through the native wttr.in API, this operation is `GET /[:location]` (base URL `https://wttr.in`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-compact-weather-forecast-json.md) for the provider-specific parameters and requirements.

