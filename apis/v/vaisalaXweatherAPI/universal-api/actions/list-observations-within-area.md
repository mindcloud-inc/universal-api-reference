# Vaisala Xweather: List Observations Within Area

Retrieves observations within an area from Vaisala Xweather API.

```
GET https://connect.mindcloud.co/v1/universal/vaisalaXweatherAPI/latest/actions/list-observations-within-area
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vaisala Xweather `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vaisalaXweatherAPI/latest/actions/list-observations-within-area?connectionId=$CONNECTION_ID&p=47.6062%2C-122.3321" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "p": "47.6062,-122.3321"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vaisalaXweatherAPI/latest/actions/list-observations-within-area?${params}`, {
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
| `p` | string | yes | Point, radius, or area geometry for the observations lookup. Example: `47.6062,-122.3321`. |
| `radius` | string | no | Radius around the point or area center. Example: `25mi`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dataSource": "string",
      "id": "string",
      "loc": {},
      "ob": {},
      "obDateTime": "2026-05-07T12:00:00.000Z",
      "obTimestamp": 1,
      "place": {},
      "profile": {},
      "raw": "string",
      "relativeTo": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dataSource` | string |  |
| `id` | string |  |
| `loc` | object |  |
| `ob` | object |  |
| `obDateTime` | date |  |
| `obTimestamp` | number |  |
| `place` | object |  |
| `profile` | object |  |
| `raw` | string |  |
| `relativeTo` | object |  |

## Native endpoint

Through the native Vaisala Xweather API, this operation is `GET /observations/within` (base URL `https://data.api.xweather.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-observations-within-area.md) for the provider-specific parameters and requirements.

