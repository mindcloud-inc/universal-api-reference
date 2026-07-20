# TVMaze Schedule: Get Show With Images

Retrieves a TVMaze show with embedded images.

```
GET https://connect.mindcloud.co/v1/universal/tVMazeSchedule/latest/actions/get-show-with-images
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TVMaze Schedule `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tVMazeSchedule/latest/actions/get-show-with-images?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tVMazeSchedule/latest/actions/get-show-with-images?${params}`, {
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
| `id` | number | yes | TVMaze show ID. Example: `1`. |

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
      "webChannel": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_embedded` | object |  |
| `_links` | object |  |
| `averageRuntime` | number |  |
| `ended` | string |  |
| `externals` | object |  |
| `genres` | array<string> |  |
| `id` | number |  |
| `image` | object |  |
| `language` | string |  |
| `name` | string |  |
| `network` | object |  |
| `officialSite` | string |  |
| `premiered` | string |  |
| `rating` | object |  |
| `runtime` | number |  |
| `schedule` | object |  |
| `status` | string |  |
| `summary` | string |  |
| `type` | string |  |
| `updated` | number |  |
| `url` | string |  |
| `webChannel` | object |  |

## Native endpoint

Through the native TVMaze Schedule API, this operation is `GET /shows/{{id}}` (base URL `https://api.tvmaze.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-show-with-images.md) for the provider-specific parameters and requirements.

