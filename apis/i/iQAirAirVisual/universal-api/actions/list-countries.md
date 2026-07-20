# IQAir AirVisual: List Countries



```
GET https://connect.mindcloud.co/v1/universal/iQAirAirVisual/latest/actions/list-countries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IQAir AirVisual `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iQAirAirVisual/latest/actions/list-countries?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iQAirAirVisual/latest/actions/list-countries?${params}`, {
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
      "country": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `country` | string | Country name returned by the AirVisual countries endpoint. |

## Native endpoint

Through the native IQAir AirVisual API, this operation is `GET /v2/countries` (base URL `https://api.airvisual.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-countries.md) for the provider-specific parameters and requirements.

