# TVMaze Schedule: Get Person With Guest Cast Credits

Retrieves a TVMaze person with embedded guest cast credits.

```
GET https://connect.mindcloud.co/v1/universal/tVMazeSchedule/latest/actions/get-person-with-guest-cast-credits
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TVMaze Schedule `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tVMazeSchedule/latest/actions/get-person-with-guest-cast-credits?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tVMazeSchedule/latest/actions/get-person-with-guest-cast-credits?${params}`, {
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
| `id` | number | yes | TVMaze person ID. Example: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_embedded": {},
      "_links": {},
      "birthday": "string",
      "country": {},
      "deathday": "string",
      "gender": "string",
      "id": 1,
      "image": {},
      "name": "Ava Chen",
      "updated": 1,
      "url": "https://example.com"
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
| `birthday` | string |  |
| `country` | object |  |
| `deathday` | string |  |
| `gender` | string |  |
| `id` | number |  |
| `image` | object |  |
| `name` | string |  |
| `updated` | number |  |
| `url` | string |  |

## Native endpoint

Through the native TVMaze Schedule API, this operation is `GET /people/{{id}}` (base URL `https://api.tvmaze.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-person-with-guest-cast-credits.md) for the provider-specific parameters and requirements.

