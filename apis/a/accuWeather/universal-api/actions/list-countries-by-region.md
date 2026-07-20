# AccuWeather: List Countries By Region

Lists the countries in AccuWeather for a region.

```
GET https://connect.mindcloud.co/v1/universal/accuWeather/latest/actions/list-countries-by-region
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AccuWeather `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/accuWeather/latest/actions/list-countries-by-region?connectionId=$CONNECTION_ID&regionCode=NAM" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "regionCode": "NAM"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/accuWeather/latest/actions/list-countries-by-region?${params}`, {
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
| `regionCode` | string | yes | Required AccuWeather region code. Default: `NAM`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "EnglishName": "Ava Chen",
      "ID": "string",
      "LocalizedName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `EnglishName` | string |  |
| `ID` | string |  |
| `LocalizedName` | string |  |

## Native endpoint

Through the native AccuWeather API, this operation is `GET /locations/v1/countries/:regionCode` (base URL `https://dataservice.accuweather.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-countries-by-region.md) for the provider-specific parameters and requirements.

