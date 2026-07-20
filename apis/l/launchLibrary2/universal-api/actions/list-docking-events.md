# Launch Library 2: List Docking Events



```
GET https://connect.mindcloud.co/v1/universal/launchLibrary2/latest/actions/list-docking-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Launch Library 2 `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/launchLibrary2/latest/actions/list-docking-events?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/launchLibrary2/latest/actions/list-docking-events?${params}`, {
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
      "departure": "2026-05-07T12:00:00.000Z",
      "docking": "2026-05-07T12:00:00.000Z",
      "docking_location": {
        "name": "Ava Chen"
      },
      "flight_vehicle_chaser": {
        "spacecraft": {
          "name": "Ava Chen"
        }
      },
      "flight_vehicle_target": {
        "spacecraft": {
          "name": "Ava Chen"
        }
      },
      "id": 1,
      "space_station_target": {
        "name": "Ava Chen"
      },
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `departure` | date |  |
| `docking` | date |  |
| `docking_location.name` | string |  |
| `flight_vehicle_chaser.spacecraft.name` | string |  |
| `flight_vehicle_target.spacecraft.name` | string |  |
| `id` | number |  |
| `space_station_target.name` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Launch Library 2 API, this operation is `GET docking_events/` (base URL `https://ll.thespacedevs.com/2.3.0/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-docking-events.md) for the provider-specific parameters and requirements.

