# TVMaze Schedule: Get Episode By Number

Retrieves a TVMaze episode by season and number.

```
GET https://connect.mindcloud.co/v1/universal/tVMazeSchedule/latest/actions/get-episode-by-number
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TVMaze Schedule `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tVMazeSchedule/latest/actions/get-episode-by-number?connectionId=$CONNECTION_ID&id=1&season=1&number=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1",
  "season": "1",
  "number": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tVMazeSchedule/latest/actions/get-episode-by-number?${params}`, {
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
| `season` | number | yes | Required season number. |
| `number` | number | yes | Required episode number within the season. |

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

Through the native TVMaze Schedule API, this operation is `GET /shows/{{id}}/episodebynumber` (base URL `https://api.tvmaze.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-episode-by-number.md) for the provider-specific parameters and requirements.

