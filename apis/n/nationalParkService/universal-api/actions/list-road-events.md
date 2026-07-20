# National Park Service: List Road Events

Retrieves road events from National Park Service.

```
GET https://connect.mindcloud.co/v1/universal/nationalParkService/latest/actions/list-road-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a National Park Service `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nationalParkService/latest/actions/list-road-events?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nationalParkService/latest/actions/list-road-events?${params}`, {
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
| `parkCode` | string | no | NPS park code. |
| `type` | string | no | Road event type, such as incident or workzone. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "features": [
        {}
      ],
      "road_event_feed_info": {},
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `features` | array<object> |  |
| `road_event_feed_info` | object |  |
| `type` | string |  |

## Native endpoint

Through the native National Park Service API, this operation is `GET /roadevents` (base URL `https://developer.nps.gov/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-road-events.md) for the provider-specific parameters and requirements.

