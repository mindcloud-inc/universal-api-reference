# OpenWeather: Geocode Location by Name

Finds matching OpenWeather locations by name.

```
GET https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/geocode-location-by-name
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenWeather `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/geocode-location-by-name?connectionId=$CONNECTION_ID&q=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "q": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/geocode-location-by-name?${params}`, {
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
| `q` | string | yes | Location name to geocode. |
| `limit` | number | no | Maximum number of matching locations to return. Default: `5`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "country": "string",
      "lat": 1,
      "local_names": {},
      "lon": 1,
      "name": "Ava Chen",
      "state": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `country` | string | Country code. |
| `lat` | number | Latitude of the matched location. |
| `local_names` | object | Localized names keyed by language code. |
| `lon` | number | Longitude of the matched location. |
| `name` | string | Resolved location name. |
| `state` | string | State or region name when available. |

## Native endpoint

Through the native OpenWeather API, this operation is `GET /geo/1.0/direct` (base URL `https://api.openweathermap.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/geocode-location-by-name.md) for the provider-specific parameters and requirements.

