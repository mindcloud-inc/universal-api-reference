# TVMaze Schedule: List Episodes By Date

Retrieves TVMaze episodes for a show by airdate.

```
GET https://connect.mindcloud.co/v1/universal/tVMazeSchedule/latest/actions/list-episodes-by-date
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TVMaze Schedule `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tVMazeSchedule/latest/actions/list-episodes-by-date?connectionId=$CONNECTION_ID&id=1&date=YYYY-MM-DD" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1",
  "date": "YYYY-MM-DD"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tVMazeSchedule/latest/actions/list-episodes-by-date?${params}`, {
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
| `date` | string | yes | Required TVMaze airdate in YYYY-MM-DD format. Example: `YYYY-MM-DD`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "airdate": "2026-05-07T12:00:00.000Z",
      "airtime": "string",
      "id": 1,
      "image": {},
      "name": "Ava Chen",
      "number": 1,
      "rating": {},
      "runtime": 1,
      "season": 1,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `airdate` | date | Air date. |
| `airtime` | string | Air time. |
| `id` | number | TVmaze episode ID. |
| `image` | object | Image object. |
| `name` | string | Episode name. |
| `number` | number | Episode number. |
| `rating` | object | Rating object. |
| `runtime` | number | Runtime in minutes. |
| `season` | number | Season number. |
| `url` | string | Episode URL. |

## Native endpoint

Through the native TVMaze Schedule API, this operation is `GET /shows/{{id}}/episodesbydate` (base URL `https://api.tvmaze.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-episodes-by-date.md) for the provider-specific parameters and requirements.

