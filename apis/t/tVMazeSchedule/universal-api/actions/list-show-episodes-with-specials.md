# TVMaze Schedule: List Show Episodes With Specials

Retrieves all TVMaze show episodes including specials.

```
GET https://connect.mindcloud.co/v1/universal/tVMazeSchedule/latest/actions/list-show-episodes-with-specials
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TVMaze Schedule `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tVMazeSchedule/latest/actions/list-show-episodes-with-specials?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tVMazeSchedule/latest/actions/list-show-episodes-with-specials?${params}`, {
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
      "_links": {},
      "airdate": "string",
      "airstamp": "string",
      "airtime": "string",
      "id": 1,
      "image": {},
      "name": "Ava Chen",
      "number": 1,
      "rating": {},
      "runtime": 1,
      "season": 1,
      "summary": "string",
      "type": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_links` | object |  |
| `airdate` | string |  |
| `airstamp` | string |  |
| `airtime` | string |  |
| `id` | number |  |
| `image` | object |  |
| `name` | string |  |
| `number` | number |  |
| `rating` | object |  |
| `runtime` | number |  |
| `season` | number |  |
| `summary` | string |  |
| `type` | string |  |
| `url` | string |  |

## Native endpoint

Through the native TVMaze Schedule API, this operation is `GET /shows/{{id}}/episodes` (base URL `https://api.tvmaze.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-show-episodes-with-specials.md) for the provider-specific parameters and requirements.

