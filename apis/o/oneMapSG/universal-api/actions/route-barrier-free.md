# OneMap SG: Route (Barrier-Free)

Retrieves a barrier-free route from OneMap SG.

```
GET https://connect.mindcloud.co/v1/universal/oneMapSG/latest/actions/route-barrier-free
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OneMap SG `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneMapSG/latest/actions/route-barrier-free?connectionId=$CONNECTION_ID&start=1.2871536%2C103.8147604&end=1.2874700%2C103.8183600" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "start": "1.2871536,103.8147604",
  "end": "1.2874700,103.8183600"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oneMapSG/latest/actions/route-barrier-free?${params}`, {
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
| `start` | string | yes | The start location as latitude and longitude. Example: `1.2871536,103.8147604`. |
| `end` | string | yes | The destination location as latitude and longitude. Example: `1.2874700,103.8183600`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "legs": [
        {}
      ],
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
| `legs` | array<object> | The route leg breakdown returned by the barrier-free service. |
| `route_geometry` | string | The encoded route geometry returned by the barrier-free routing service. |
| `route_instructions` | array<object> | The step-by-step barrier-free route instructions. |
| `route_name` | array<string> | The route segment names returned by OneMap. |
| `route_summary` | object | The total distance and time summary for the route. |
| `status` | number | The numeric route status returned by OneMap. |
| `status_message` | string | The provider status message for the barrier-free route request. |

## Native endpoint

Through the native OneMap SG API, this operation is `GET /api/bfa/routingsvc/route` (base URL `https://www.onemap.gov.sg`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/route-barrier-free.md) for the provider-specific parameters and requirements.

