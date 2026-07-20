# AccuWeather: Get Daily Index Metadata

Retrieves daily index metadata from AccuWeather.

```
GET https://connect.mindcloud.co/v1/universal/accuWeather/latest/actions/get-daily-index-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AccuWeather `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/accuWeather/latest/actions/get-daily-index-metadata?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/accuWeather/latest/actions/get-daily-index-metadata?${params}`, {
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
| `ID` | string | no | Required index ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Description": "string",
      "ID": 1,
      "Name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Description` | string |  |
| `ID` | number |  |
| `Name` | string |  |

## Native endpoint

Through the native AccuWeather API, this operation is `GET /indices/v1/daily/:ID` (base URL `https://dataservice.accuweather.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-daily-index-metadata.md) for the provider-specific parameters and requirements.

