# TVMaze Schedule: Get Person

Retrieves a person from TVMaze by ID.

```
GET https://connect.mindcloud.co/v1/universal/tVMazeSchedule/latest/actions/get-person
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TVMaze Schedule `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tVMazeSchedule/latest/actions/get-person?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tVMazeSchedule/latest/actions/get-person?${params}`, {
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
| `id` | number | yes | Required TVmaze person ID. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `embed` | string | no | Optional embedded resource name, such as castcredits. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_embedded": {},
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
| `_embedded` | object | Optional embedded resources. |
| `birthday` | date | Birth date. |
| `country` | object | Country object. |
| `deathday` | date | Death date, if applicable. |
| `gender` | string | Gender value. |
| `id` | number | TVmaze person ID. |
| `image` | object | Image object. |
| `name` | string | Person name. |
| `url` | string | TVmaze person URL. |

## Native endpoint

Through the native TVMaze Schedule API, this operation is `GET /people/{{id}}` (base URL `https://api.tvmaze.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-person.md) for the provider-specific parameters and requirements.

