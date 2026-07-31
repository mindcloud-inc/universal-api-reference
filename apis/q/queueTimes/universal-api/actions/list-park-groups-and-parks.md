# Queue Times: List Park Groups and Parks



```
GET https://connect.mindcloud.co/v1/universal/queueTimes/latest/actions/list-park-groups-and-parks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Queue Times `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/queueTimes/latest/actions/list-park-groups-and-parks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/queueTimes/latest/actions/list-park-groups-and-parks?${params}`, {
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
      "": [
        {
          "id": 1,
          "name": "Ava Chen",
          "parks": [
            {
              "continent": "string",
              "country": "string",
              "id": 1,
              "latitude": "string",
              "longitude": "string",
              "name": "Ava Chen",
              "timezone": "string"
            }
          ]
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `[]` | array<object> |  |
| `[].id` | number |  |
| `[].name` | string |  |
| `[].parks` | array<object> |  |
| `[].parks[].continent` | string |  |
| `[].parks[].country` | string |  |
| `[].parks[].id` | number |  |
| `[].parks[].latitude` | string |  |
| `[].parks[].longitude` | string |  |
| `[].parks[].name` | string |  |
| `[].parks[].timezone` | string |  |

## Native endpoint

Through the native Queue Times API, this operation is `GET /parks.json` (base URL `https://queue-times.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-park-groups-and-parks.md) for the provider-specific parameters and requirements.

