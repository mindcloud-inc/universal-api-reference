# TVMaze Schedule: List Schedule

Retrieves the TV schedule from TVMaze.

```
GET https://connect.mindcloud.co/v1/universal/tVMazeSchedule/latest/actions/list-schedule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TVMaze Schedule `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tVMazeSchedule/latest/actions/list-schedule?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tVMazeSchedule/latest/actions/list-schedule?${params}`, {
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
| `country` | string | no | Optional ISO 3166-1 country code; defaults to US. |
| `date` | string | no | Schedule date in TVMaze YYYY-MM-DD format. Example: `YYYY-MM-DD`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "airdate": "2026-05-07T12:00:00.000Z",
      "airstamp": "2026-05-07T12:00:00.000Z",
      "airtime": "string",
      "id": 1,
      "name": "Ava Chen",
      "number": 1,
      "rating": {},
      "runtime": 1,
      "season": 1,
      "show": {},
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
| `airstamp` | date | Air timestamp. |
| `airtime` | string | Local air time. |
| `id` | number | TVmaze episode ID. |
| `name` | string | Episode name. |
| `number` | number | Episode number. |
| `rating` | object | Rating object. |
| `runtime` | number | Runtime in minutes. |
| `season` | number | Season number. |
| `show` | object | Embedded show object. |
| `url` | string | TVmaze episode URL. |

## Native endpoint

Through the native TVMaze Schedule API, this operation is `GET /schedule` (base URL `https://api.tvmaze.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-schedule.md) for the provider-specific parameters and requirements.

