# TVMaze Schedule: List Episode Guest Cast

Retrieves guest cast for a TVMaze episode.

```
GET https://connect.mindcloud.co/v1/universal/tVMazeSchedule/latest/actions/list-episode-guest-cast
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TVMaze Schedule `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tVMazeSchedule/latest/actions/list-episode-guest-cast?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tVMazeSchedule/latest/actions/list-episode-guest-cast?${params}`, {
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
| `id` | number | yes | Required TVmaze episode ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "character": {},
      "person": {},
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
| `character` | object | Character object. |
| `person` | object | Guest cast person object. |
| `self` | boolean | Whether the person appears as themself. |
| `voice` | boolean | Whether this is a voice role. |

## Native endpoint

Through the native TVMaze Schedule API, this operation is `GET /episodes/{{id}}/guestcast` (base URL `https://api.tvmaze.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-episode-guest-cast.md) for the provider-specific parameters and requirements.

