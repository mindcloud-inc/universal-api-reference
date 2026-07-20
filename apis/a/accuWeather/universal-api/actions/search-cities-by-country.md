# AccuWeather: Search Cities By Country

Finds cities in AccuWeather by country and text.

```
GET https://connect.mindcloud.co/v1/universal/accuWeather/latest/actions/search-cities-by-country
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AccuWeather `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/accuWeather/latest/actions/search-cities-by-country?connectionId=$CONNECTION_ID&countryCode=US&q=San" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "countryCode": "US",
  "q": "San"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/accuWeather/latest/actions/search-cities-by-country?${params}`, {
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
| `countryCode` | string | yes | Required AccuWeather country code. Default: `US`. |
| `q` | string | yes | Required city search query text. Default: `San`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "AdministrativeArea": {
        "ID": "string"
      },
      "Country": {
        "ID": "string"
      },
      "EnglishName": "Ava Chen",
      "Key": "string",
      "LocalizedName": "Ava Chen",
      "Rank": 1,
      "Type": "string",
      "Version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `AdministrativeArea.ID` | string |  |
| `Country.ID` | string |  |
| `EnglishName` | string |  |
| `Key` | string |  |
| `LocalizedName` | string |  |
| `Rank` | number |  |
| `Type` | string |  |
| `Version` | number |  |

## Native endpoint

Through the native AccuWeather API, this operation is `GET /locations/v1/cities/:countryCode/search` (base URL `https://dataservice.accuweather.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-cities-by-country.md) for the provider-specific parameters and requirements.

