# Control D: List Proxies

Retrieves proxies from Control D.

```
GET https://connect.mindcloud.co/v1/universal/controlD/latest/actions/list-proxies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Control D `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/controlD/latest/actions/list-proxies?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/controlD/latest/actions/list-proxies?${params}`, {
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
      "city": "string",
      "country": "string",
      "country_name": "Ava Chen",
      "gps_lat": 1,
      "gps_long": 1,
      "PK": "string",
      "uid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `city` | string |  |
| `country` | string |  |
| `country_name` | string |  |
| `gps_lat` | number |  |
| `gps_long` | number |  |
| `PK` | string |  |
| `uid` | string |  |

## Native endpoint

Through the native Control D API, this operation is `GET /proxies` (base URL `https://api.controld.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-proxies.md) for the provider-specific parameters and requirements.

