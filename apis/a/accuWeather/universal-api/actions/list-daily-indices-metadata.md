# AccuWeather: List Daily Indices Metadata

Lists daily indices metadata in AccuWeather.

```
GET https://connect.mindcloud.co/v1/universal/accuWeather/latest/actions/list-daily-indices-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AccuWeather `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/accuWeather/latest/actions/list-daily-indices-metadata?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/accuWeather/latest/actions/list-daily-indices-metadata?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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

Through the native AccuWeather API, this operation is `GET /indices/v1/daily` (base URL `https://dataservice.accuweather.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-daily-indices-metadata.md) for the provider-specific parameters and requirements.

