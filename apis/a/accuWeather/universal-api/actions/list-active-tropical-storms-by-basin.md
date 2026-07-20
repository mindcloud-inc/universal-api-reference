# AccuWeather: List Active Tropical Storms By Basin

Lists active tropical storms in AccuWeather by basin.

```
GET https://connect.mindcloud.co/v1/universal/accuWeather/latest/actions/list-active-tropical-storms-by-basin
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AccuWeather `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/accuWeather/latest/actions/list-active-tropical-storms-by-basin?connectionId=$CONNECTION_ID&basin=AL" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "basin": "AL"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/accuWeather/latest/actions/list-active-tropical-storms-by-basin?${params}`, {
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
| `basin` | string | yes | Required tropical basin code. Default: `AL`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Basin": "string",
      "GovernmentID": 1,
      "Name": "Ava Chen",
      "Year": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Basin` | string |  |
| `GovernmentID` | number |  |
| `Name` | string |  |
| `Year` | number |  |

## Native endpoint

Through the native AccuWeather API, this operation is `GET /tropical/v1/gov/storms/active/:basin` (base URL `https://dataservice.accuweather.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-active-tropical-storms-by-basin.md) for the provider-specific parameters and requirements.

