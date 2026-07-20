# TVMaze Schedule: List Show Seasons

Retrieves seasons for a TVMaze show.

```
GET https://connect.mindcloud.co/v1/universal/tVMazeSchedule/latest/actions/list-show-seasons
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TVMaze Schedule `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tVMazeSchedule/latest/actions/list-show-seasons?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tVMazeSchedule/latest/actions/list-show-seasons?${params}`, {
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
| `id` | number | yes | Required TVmaze show ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "endDate": "2026-05-07T12:00:00.000Z",
      "episodeOrder": 1,
      "id": 1,
      "name": "Ava Chen",
      "network": {},
      "number": 1,
      "premiereDate": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com",
      "webChannel": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `endDate` | date | Season end date. |
| `episodeOrder` | number | Expected episode count. |
| `id` | number | Season ID. |
| `name` | string | Season name. |
| `network` | object | Network object. |
| `number` | number | Season number. |
| `premiereDate` | date | Season premiere date. |
| `url` | string | Season URL. |
| `webChannel` | object | Web channel object. |

## Native endpoint

Through the native TVMaze Schedule API, this operation is `GET /shows/{{id}}/seasons` (base URL `https://api.tvmaze.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-show-seasons.md) for the provider-specific parameters and requirements.

