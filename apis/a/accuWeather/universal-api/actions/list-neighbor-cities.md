# AccuWeather: List Neighbor Cities

Lists neighboring cities in AccuWeather for a location.

```
GET https://connect.mindcloud.co/v1/universal/accuWeather/latest/actions/list-neighbor-cities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AccuWeather `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/accuWeather/latest/actions/list-neighbor-cities?connectionId=$CONNECTION_ID&locationKey=349727" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "locationKey": "349727"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/accuWeather/latest/actions/list-neighbor-cities?${params}`, {
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

Through the native AccuWeather API, this operation is `GET /locations/v1/cities/neighbors/:locationKey` (base URL `https://dataservice.accuweather.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-neighbor-cities.md) for the provider-specific parameters and requirements.

