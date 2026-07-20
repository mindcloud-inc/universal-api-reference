# AccuWeather: Get Location By Key

Retrieves a location from AccuWeather by key.

```
GET https://connect.mindcloud.co/v1/universal/accuWeather/latest/actions/get-location-by-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AccuWeather `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/accuWeather/latest/actions/get-location-by-key?connectionId=$CONNECTION_ID&locationKey=349727" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "locationKey": "349727"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/accuWeather/latest/actions/get-location-by-key?${params}`, {
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
| `locationKey` | string | yes | Required AccuWeather location key. Default: `349727`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "AdministrativeArea": {
        "ID": "string",
        "LocalizedName": "Ava Chen"
      },
      "Country": {
        "ID": "string",
        "LocalizedName": "Ava Chen"
      },
      "EnglishName": "Ava Chen",
      "GeoPosition": {
        "Latitude": 1,
        "Longitude": 1
      },
      "Key": "string",
      "LocalizedName": "Ava Chen",
      "Rank": 1,
      "TimeZone": {
        "Code": "string"
      },
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
| `AdministrativeArea.LocalizedName` | string |  |
| `Country.ID` | string |  |
| `Country.LocalizedName` | string |  |
| `EnglishName` | string |  |
| `GeoPosition.Latitude` | number |  |
| `GeoPosition.Longitude` | number |  |
| `Key` | string |  |
| `LocalizedName` | string |  |
| `Rank` | number |  |
| `TimeZone.Code` | string |  |
| `Type` | string |  |
| `Version` | number |  |

## Native endpoint

Through the native AccuWeather API, this operation is `GET /locations/v1/:locationKey` (base URL `https://dataservice.accuweather.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-location-by-key.md) for the provider-specific parameters and requirements.

