# TVMaze Schedule: Search Single Show

Finds a single show in TVMaze by name.

```
GET https://connect.mindcloud.co/v1/universal/tVMazeSchedule/latest/actions/search-single-show
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TVMaze Schedule `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tVMazeSchedule/latest/actions/search-single-show?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tVMazeSchedule/latest/actions/search-single-show?${params}`, {
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
| `query` | string | yes | Required show search query. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `embed` | string | no | Optional embedded resource name, such as episodes or cast. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_embedded": {},
      "genres": [
        "string"
      ],
      "id": 1,
      "language": "string",
      "name": "Ava Chen",
      "network": {},
      "premiered": "2026-05-07T12:00:00.000Z",
      "rating": {},
      "status": "string",
      "type": "string",
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
| `_embedded` | object | Optional embedded resources. |
| `genres` | array<string> | Show genres. |
| `id` | number | TVmaze show ID. |
| `language` | string | Primary language. |
| `name` | string | Show name. |
| `network` | object | Network object. |
| `premiered` | date | Premiere date. |
| `rating` | object | Rating object. |
| `status` | string | Show status. |
| `type` | string | Show type. |
| `url` | string | TVmaze show URL. |
| `webChannel` | object | Web channel object. |

## Native endpoint

Through the native TVMaze Schedule API, this operation is `GET /singlesearch/shows` (base URL `https://api.tvmaze.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-single-show.md) for the provider-specific parameters and requirements.

