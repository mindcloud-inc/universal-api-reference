# AccuWeather: Autocomplete Points Of Interest

Finds points of interest in AccuWeather by autocomplete.

```
GET https://connect.mindcloud.co/v1/universal/accuWeather/latest/actions/autocomplete-points-of-interest
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AccuWeather `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/accuWeather/latest/actions/autocomplete-points-of-interest?connectionId=$CONNECTION_ID&q=Central" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "q": "Central"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/accuWeather/latest/actions/autocomplete-points-of-interest?${params}`, {
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
| `q` | string | yes | Required autocomplete query text. Default: `Central`. |

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

Through the native AccuWeather API, this operation is `GET /locations/v1/pois/autocomplete` (base URL `https://dataservice.accuweather.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/autocomplete-points-of-interest.md) for the provider-specific parameters and requirements.

