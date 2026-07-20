# AccuWeather: List Top Cities

Lists top cities in AccuWeather by group.

```
GET https://connect.mindcloud.co/v1/universal/accuWeather/latest/actions/list-top-cities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AccuWeather `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/accuWeather/latest/actions/list-top-cities?connectionId=$CONNECTION_ID&group=50" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "group": "50"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/accuWeather/latest/actions/list-top-cities?${params}`, {
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
| `group` | string | yes | Required top-city group number. Default: `50`. |

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
      "Rank": 1
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

## Native endpoint

Through the native AccuWeather API, this operation is `GET /locations/v1/topcities/:group` (base URL `https://dataservice.accuweather.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-top-cities.md) for the provider-specific parameters and requirements.

