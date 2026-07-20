# AccuWeather: Search Admin Areas Globally

Finds admin areas in AccuWeather by global search.

```
GET https://connect.mindcloud.co/v1/universal/accuWeather/latest/actions/search-admin-areas-globally
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AccuWeather `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/accuWeather/latest/actions/search-admin-areas-globally?connectionId=$CONNECTION_ID&q=California" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "q": "California"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/accuWeather/latest/actions/search-admin-areas-globally?${params}`, {
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
| `q` | string | yes | Required search query text. Default: `California`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "EnglishName": "Ava Chen",
      "EnglishType": "string",
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
| `EnglishType` | string |  |
| `ID` | string |  |
| `LocalizedName` | string |  |

## Native endpoint

Through the native AccuWeather API, this operation is `GET /locations/v1/adminareas/search` (base URL `https://dataservice.accuweather.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-admin-areas-globally.md) for the provider-specific parameters and requirements.

