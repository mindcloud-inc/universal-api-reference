# TVMaze Schedule: Search Single Show With Episodes

Finds a single TVMaze show by name with episodes.

```
GET https://connect.mindcloud.co/v1/universal/tVMazeSchedule/latest/actions/search-single-show-with-episodes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TVMaze Schedule `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tVMazeSchedule/latest/actions/search-single-show-with-episodes?connectionId=$CONNECTION_ID&query=girls" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "girls"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tVMazeSchedule/latest/actions/search-single-show-with-episodes?${params}`, {
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
| `query` | string | yes | Show name query to search for. Example: `girls`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_embedded": {},
      "_links": {},
      "averageRuntime": 1,
      "ended": "string",
      "externals": {},
      "genres": [
        "string"
      ],
      "id": 1,
      "image": {},
      "language": "string",
      "name": "Ava Chen",
      "network": {},
      "officialSite": "string",
      "premiered": "string",
      "rating": {},
      "runtime": 1,
      "schedule": {},
      "status": "string",
      "summary": "string",
      "type": "string",
      "updated": 1,
      "url": "https://example.com",
      "webChannel": {},
      "weight": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_embedded` | object | Embedded episodes collection. |
| `_links` | object | HAL links. |
| `averageRuntime` | number | Average episode runtime in minutes. |
| `ended` | string | End date. |
| `externals` | object | External identifiers. |
| `genres` | array<string> | Show genres. |
| `id` | number | TVMaze show ID. |
| `image` | object | Image URLs. |
| `language` | string | Primary language. |
| `name` | string | Show name. |
| `network` | object | Network details. |
| `officialSite` | string | Official site URL. |
| `premiered` | string | Premiere date. |
| `rating` | object | Rating details. |
| `runtime` | number | Episode runtime in minutes. |
| `schedule` | object | Airtime and days. |
| `status` | string | Show status. |
| `summary` | string | HTML summary. |
| `type` | string | Show type. |
| `updated` | number | Last update timestamp. |
| `url` | string | TVMaze show URL. |
| `webChannel` | object | Web channel details. |
| `weight` | number | TVMaze weight. |

## Native endpoint

Through the native TVMaze Schedule API, this operation is `GET /singlesearch/shows` (base URL `https://api.tvmaze.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-single-show-with-episodes.md) for the provider-specific parameters and requirements.

