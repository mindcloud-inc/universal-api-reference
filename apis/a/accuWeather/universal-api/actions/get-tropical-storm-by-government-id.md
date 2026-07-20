# AccuWeather: Get Tropical Storm By Government Id

Retrieves a tropical storm from AccuWeather by year, basin, and government ID.

```
GET https://connect.mindcloud.co/v1/universal/accuWeather/latest/actions/get-tropical-storm-by-government-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AccuWeather `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/accuWeather/latest/actions/get-tropical-storm-by-government-id?connectionId=$CONNECTION_ID&basin=AL&govId=2&year=2024" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "basin": "AL",
  "govId": "2",
  "year": "2024"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/accuWeather/latest/actions/get-tropical-storm-by-government-id?${params}`, {
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
| `govId` | string | yes | Required government storm ID. Default: `2`. |
| `year` | string | yes | Required four-digit year. Default: `2024`. |

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

Through the native AccuWeather API, this operation is `GET /tropical/v1/gov/storms/:year/:basin/:govId` (base URL `https://dataservice.accuweather.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-tropical-storm-by-government-id.md) for the provider-specific parameters and requirements.

