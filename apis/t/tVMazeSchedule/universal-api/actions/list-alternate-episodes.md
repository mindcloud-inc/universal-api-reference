# TVMaze Schedule: List Alternate Episodes

Retrieves alternate episodes for a TVMaze list.

```
GET https://connect.mindcloud.co/v1/universal/tVMazeSchedule/latest/actions/list-alternate-episodes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TVMaze Schedule `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tVMazeSchedule/latest/actions/list-alternate-episodes?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tVMazeSchedule/latest/actions/list-alternate-episodes?${params}`, {
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
| `id` | number | yes | Required TVmaze alternate list ID. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `embed` | string | no | Optional embedded resource name, such as episodes. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_embedded": {},
      "airdate": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "name": "Ava Chen",
      "number": 1,
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
| `_embedded` | object | Optional embedded resources. |
| `airdate` | date | Air date. |
| `id` | number | Alternate episode ID. |
| `name` | string | Episode name. |
| `number` | number | Episode number. |
| `season` | number | Season number. |
| `url` | string | Episode URL. |

## Native endpoint

Through the native TVMaze Schedule API, this operation is `GET /alternatelists/{{id}}/alternateepisodes` (base URL `https://api.tvmaze.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-alternate-episodes.md) for the provider-specific parameters and requirements.

