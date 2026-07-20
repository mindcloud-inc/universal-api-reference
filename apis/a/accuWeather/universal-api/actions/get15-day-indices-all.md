# AccuWeather: Get 15 Day Indices All

Retrieves all 15-day indices from AccuWeather.

```
GET https://connect.mindcloud.co/v1/universal/accuWeather/latest/actions/get15-day-indices-all
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AccuWeather `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/accuWeather/latest/actions/get15-day-indices-all?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/accuWeather/latest/actions/get15-day-indices-all?${params}`, {
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
| `locationKey` | string | no | Required AccuWeather location key. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Category": "string",
      "LocalDateTime": "string",
      "Name": "Ava Chen",
      "Value": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Category` | string |  |
| `LocalDateTime` | string |  |
| `Name` | string |  |
| `Value` | number |  |

## Native endpoint

Through the native AccuWeather API, this operation is `GET /indices/v1/daily/15day/:locationKey` (base URL `https://dataservice.accuweather.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get15-day-indices-all.md) for the provider-specific parameters and requirements.

