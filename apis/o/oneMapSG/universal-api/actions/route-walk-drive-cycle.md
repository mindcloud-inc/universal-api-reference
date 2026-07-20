# OneMap SG: Route (Walk, Drive, or Cycle)

Retrieves a walking, driving, or cycling route from OneMap SG.

```
GET https://connect.mindcloud.co/v1/universal/oneMapSG/latest/actions/route-walk-drive-cycle
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OneMap SG `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneMapSG/latest/actions/route-walk-drive-cycle?connectionId=$CONNECTION_ID&start=1.319728%2C103.8421&end=1.319728905%2C103.8421581" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "start": "1.319728,103.8421",
  "end": "1.319728905,103.8421581"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oneMapSG/latest/actions/route-walk-drive-cycle?${params}`, {
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
| `start` | string | yes | The start location as latitude and longitude. Example: `1.319728,103.8421`. |
| `end` | string | yes | The destination location as latitude and longitude. Example: `1.319728905,103.8421581`. |
| `routeType` | string | no | The route type such as walk, drive, or cycle. Default: `walk`. Example: `walk`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "route_geometry": "string",
      "route_instructions": [
        {}
      ],
      "route_name": [
        "Ava Chen"
      ],
      "route_summary": {},
      "status": 1,
      "status_message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `route_geometry` | string |  |
| `route_instructions` | array<object> |  |
| `route_name` | array<string> |  |
| `route_summary` | object |  |
| `status` | number |  |
| `status_message` | string |  |

## Native endpoint

Through the native OneMap SG API, this operation is `GET /api/public/routingsvc/route` (base URL `https://www.onemap.gov.sg`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/route-walk-drive-cycle.md) for the provider-specific parameters and requirements.

