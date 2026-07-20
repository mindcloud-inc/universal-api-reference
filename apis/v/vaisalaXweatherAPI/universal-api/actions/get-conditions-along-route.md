# Vaisala Xweather: Get Conditions Along Route

Retrieves conditions along a route from Vaisala Xweather API.

```
GET https://connect.mindcloud.co/v1/universal/vaisalaXweatherAPI/latest/actions/get-conditions-along-route
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vaisala Xweather `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vaisalaXweatherAPI/latest/actions/get-conditions-along-route?connectionId=$CONNECTION_ID&p=47.6062%2C-122.3321%3B47.6205%2C-122.3493" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "p": "47.6062,-122.3321;47.6205,-122.3493"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vaisalaXweatherAPI/latest/actions/get-conditions-along-route?${params}`, {
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
| `p` | string | yes | Semicolon-delimited route points using latitude/longitude pairs. Example: `47.6062,-122.3321;47.6205,-122.3493`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "geometry": {},
      "id": "string",
      "properties": {},
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `geometry` | object |  |
| `id` | string |  |
| `properties` | object |  |
| `type` | string |  |

## Native endpoint

Through the native Vaisala Xweather API, this operation is `GET /conditions/route` (base URL `https://data.api.xweather.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-conditions-along-route.md) for the provider-specific parameters and requirements.

