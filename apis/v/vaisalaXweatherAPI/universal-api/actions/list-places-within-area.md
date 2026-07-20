# Vaisala Xweather: List Places Within Area

Retrieves places within an area from Vaisala Xweather API.

```
GET https://connect.mindcloud.co/v1/universal/vaisalaXweatherAPI/latest/actions/list-places-within-area
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vaisala Xweather `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vaisalaXweatherAPI/latest/actions/list-places-within-area?connectionId=$CONNECTION_ID&p=47.6062%2C-122.3321" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "p": "47.6062,-122.3321"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vaisalaXweatherAPI/latest/actions/list-places-within-area?${params}`, {
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
| `p` | string | yes | Circle center, bounding box, or polygon defining the search area. Example: `47.6062,-122.3321`. |
| `radius` | string | no | Radius used with center-point within searches. Example: `25mi`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "loc": {},
      "place": {},
      "profile": {},
      "relativeTo": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `loc` | object |  |
| `place` | object |  |
| `profile` | object |  |
| `relativeTo` | object |  |

## Native endpoint

Through the native Vaisala Xweather API, this operation is `GET /places/within` (base URL `https://data.api.xweather.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-places-within-area.md) for the provider-specific parameters and requirements.

