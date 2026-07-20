# TVMaze Schedule: List People

Retrieves all person records from TVMaze.

```
GET https://connect.mindcloud.co/v1/universal/tVMazeSchedule/latest/actions/list-people
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TVMaze Schedule `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tVMazeSchedule/latest/actions/list-people?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tVMazeSchedule/latest/actions/list-people?${params}`, {
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
| `page` | number | no | Optional page number for TVmaze people index; starts at 0. Default: `0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "birthday": "2026-05-07T12:00:00.000Z",
      "country": {},
      "deathday": "2026-05-07T12:00:00.000Z",
      "gender": "string",
      "id": 1,
      "image": {},
      "name": "Ava Chen",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `birthday` | date | Birth date. |
| `country` | object | Country object. |
| `deathday` | date | Death date, if applicable. |
| `gender` | string | Gender value. |
| `id` | number | TVmaze person ID. |
| `image` | object | Image object. |
| `name` | string | Person name. |
| `url` | string | TVmaze person URL. |

## Native endpoint

Through the native TVMaze Schedule API, this operation is `GET /people` (base URL `https://api.tvmaze.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-people.md) for the provider-specific parameters and requirements.

