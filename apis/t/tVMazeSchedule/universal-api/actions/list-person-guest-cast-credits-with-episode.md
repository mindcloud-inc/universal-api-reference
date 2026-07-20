# TVMaze Schedule: List Person Guest Cast Credits With Episode

Retrieves TVMaze guest cast credits with embedded episodes.

```
GET https://connect.mindcloud.co/v1/universal/tVMazeSchedule/latest/actions/list-person-guest-cast-credits-with-episode
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TVMaze Schedule `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tVMazeSchedule/latest/actions/list-person-guest-cast-credits-with-episode?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tVMazeSchedule/latest/actions/list-person-guest-cast-credits-with-episode?${params}`, {
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
      "self": true,
      "voice": true
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
| `self` | boolean |  |
| `voice` | boolean |  |

## Native endpoint

Through the native TVMaze Schedule API, this operation is `GET /people/{{id}}/guestcastcredits` (base URL `https://api.tvmaze.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-person-guest-cast-credits-with-episode.md) for the provider-specific parameters and requirements.

