# Zubie: List Trips

Retrieves trips from Zubie.

```
GET https://connect.mindcloud.co/v1/universal/zubie/latest/actions/list-trips
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zubie `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zubie/latest/actions/list-trips?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zubie/latest/actions/list-trips?${params}`, {
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
| `vehicle_key` | string | no | Filter results to a single vehicle. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "duration_seconds": 1,
      "end_point": {},
      "key": "string",
      "start_point": {},
      "user_key": "string",
      "vehicle_key": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `duration_seconds` | number |  |
| `end_point` | object |  |
| `key` | string |  |
| `start_point` | object |  |
| `user_key` | string |  |
| `vehicle_key` | string |  |

## Native endpoint

Through the native Zubie API, this operation is `GET /trips` (base URL `https://api.zubiecar.com/api/v2/zinc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-trips.md) for the provider-specific parameters and requirements.

