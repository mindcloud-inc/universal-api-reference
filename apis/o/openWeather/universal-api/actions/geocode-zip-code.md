# OpenWeather: Geocode ZIP Code

Finds an OpenWeather location by ZIP code.

```
GET https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/geocode-zip-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenWeather `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/geocode-zip-code?connectionId=$CONNECTION_ID&zip=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "zip": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/geocode-zip-code?${params}`, {
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
| `zip` | string | yes | ZIP or postal code with country code. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "country": "string",
      "lat": 1,
      "lon": 1,
      "name": "Ava Chen",
      "zip": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `country` | string |  |
| `lat` | number |  |
| `lon` | number |  |
| `name` | string |  |
| `zip` | string |  |

## Native endpoint

Through the native OpenWeather API, this operation is `GET /geo/1.0/zip` (base URL `https://api.openweathermap.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/geocode-zip-code.md) for the provider-specific parameters and requirements.

