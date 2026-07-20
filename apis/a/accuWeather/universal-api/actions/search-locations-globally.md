# AccuWeather: Search Locations Globally

Finds locations in AccuWeather by global text search.

```
GET https://connect.mindcloud.co/v1/universal/accuWeather/latest/actions/search-locations-globally
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AccuWeather `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/accuWeather/latest/actions/search-locations-globally?connectionId=$CONNECTION_ID&q=Buenos%20Aires" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "q": "Buenos Aires"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/accuWeather/latest/actions/search-locations-globally?${params}`, {
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
| `q` | string | yes | Required search query text. Default: `Buenos Aires`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "EnglishName": "Ava Chen",
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
| `EnglishName` | string |  |
| `Key` | string |  |
| `LocalizedName` | string |  |
| `Version` | number |  |

## Native endpoint

Through the native AccuWeather API, this operation is `GET /locations/v1/search` (base URL `https://dataservice.accuweather.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-locations-globally.md) for the provider-specific parameters and requirements.

