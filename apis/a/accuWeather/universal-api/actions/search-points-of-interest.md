# AccuWeather: Search Points Of Interest

Finds points of interest in AccuWeather by text.

```
GET https://connect.mindcloud.co/v1/universal/accuWeather/latest/actions/search-points-of-interest
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AccuWeather `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/accuWeather/latest/actions/search-points-of-interest?connectionId=$CONNECTION_ID&q=Central%20Park" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "q": "Central Park"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/accuWeather/latest/actions/search-points-of-interest?${params}`, {
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
| `q` | string | yes | Required point of interest query text. Default: `Central Park`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Key": "string",
      "LocalizedName": "Ava Chen",
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
| `Key` | string |  |
| `LocalizedName` | string |  |
| `Type` | string |  |
| `Version` | number |  |

## Native endpoint

Through the native AccuWeather API, this operation is `GET /locations/v1/pois/search` (base URL `https://dataservice.accuweather.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-points-of-interest.md) for the provider-specific parameters and requirements.

