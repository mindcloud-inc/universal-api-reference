# AccuWeather: Autocomplete Cities

Finds cities in AccuWeather by autocomplete text.

```
GET https://connect.mindcloud.co/v1/universal/accuWeather/latest/actions/autocomplete-cities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AccuWeather `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/accuWeather/latest/actions/autocomplete-cities?connectionId=$CONNECTION_ID&q=San" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "q": "San"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/accuWeather/latest/actions/autocomplete-cities?${params}`, {
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
| `q` | string | yes | Required autocomplete query text. Default: `San`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "AdministrativeArea": {
        "LocalizedName": "Ava Chen"
      },
      "Country": {
        "LocalizedName": "Ava Chen"
      },
      "Key": "string",
      "LocalizedName": "Ava Chen",
      "Version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `AdministrativeArea.LocalizedName` | string |  |
| `Country.LocalizedName` | string |  |
| `Key` | string |  |
| `LocalizedName` | string |  |
| `Version` | number |  |

## Native endpoint

Through the native AccuWeather API, this operation is `GET /locations/v1/cities/autocomplete` (base URL `https://dataservice.accuweather.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/autocomplete-cities.md) for the provider-specific parameters and requirements.

