# TVMaze Schedule: Lookup Show By IMDb ID

Finds a TVMaze show by IMDb ID.

```
GET https://connect.mindcloud.co/v1/universal/tVMazeSchedule/latest/actions/lookup-show-by-imdb-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TVMaze Schedule `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tVMazeSchedule/latest/actions/lookup-show-by-imdb-id?connectionId=$CONNECTION_ID&imdbId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "imdbId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tVMazeSchedule/latest/actions/lookup-show-by-imdb-id?${params}`, {
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
| `imdbId` | string | yes | Required IMDb title ID, for example tt0944947. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "externals": {},
      "genres": [
        "string"
      ],
      "id": 1,
      "language": "string",
      "name": "Ava Chen",
      "premiered": "2026-05-07T12:00:00.000Z",
      "status": "string",
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
| `externals` | object | External provider IDs. |
| `genres` | array<string> | Show genres. |
| `id` | number | TVmaze show ID. |
| `language` | string | Primary language. |
| `name` | string | Show name. |
| `premiered` | date | Premiere date. |
| `status` | string | Show status. |
| `type` | string | Show type. |
| `url` | string | TVmaze show URL. |

## Native endpoint

Through the native TVMaze Schedule API, this operation is `GET /lookup/shows` (base URL `https://api.tvmaze.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/lookup-show-by-imdb-id.md) for the provider-specific parameters and requirements.

