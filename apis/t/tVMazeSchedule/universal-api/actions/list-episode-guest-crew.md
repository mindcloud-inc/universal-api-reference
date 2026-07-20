# TVMaze Schedule: List Episode Guest Crew

Retrieves guest crew for a TVMaze episode.

```
GET https://connect.mindcloud.co/v1/universal/tVMazeSchedule/latest/actions/list-episode-guest-crew
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TVMaze Schedule `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tVMazeSchedule/latest/actions/list-episode-guest-crew?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tVMazeSchedule/latest/actions/list-episode-guest-crew?${params}`, {
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
| `id` | number | yes | Required TVmaze episode ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "guestCrewType": "string",
      "person": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `guestCrewType` | string |  |
| `person` | object |  |

## Native endpoint

Through the native TVMaze Schedule API, this operation is `GET /episodes/{{id}}/guestcrew` (base URL `https://api.tvmaze.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-episode-guest-crew.md) for the provider-specific parameters and requirements.

