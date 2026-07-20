# AccuWeather: Get MinuteCast By Geoposition

Retrieves MinuteCast data from AccuWeather by geoposition.

```
GET https://connect.mindcloud.co/v1/universal/accuWeather/latest/actions/get-minute-cast-by-geoposition
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AccuWeather `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/accuWeather/latest/actions/get-minute-cast-by-geoposition?connectionId=$CONNECTION_ID&q=40.779%2C-73.969" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "q": "40.779,-73.969"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/accuWeather/latest/actions/get-minute-cast-by-geoposition?${params}`, {
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
| `q` | string | yes | Required geoposition as latitude,longitude. Default: `40.779,-73.969`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Link": "https://example.com",
      "Minutes": [
        {}
      ],
      "MobileLink": "https://example.com",
      "Summary": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Link` | string |  |
| `Minutes` | array<object> |  |
| `MobileLink` | string |  |
| `Summary` | string |  |

## Native endpoint

Through the native AccuWeather API, this operation is `GET /forecasts/v1/minute` (base URL `https://dataservice.accuweather.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-minute-cast-by-geoposition.md) for the provider-specific parameters and requirements.

