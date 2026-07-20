# TVMaze Schedule: List Person Cast Credits

Retrieves cast credits for a TVMaze person.

```
GET https://connect.mindcloud.co/v1/universal/tVMazeSchedule/latest/actions/list-person-cast-credits
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TVMaze Schedule `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tVMazeSchedule/latest/actions/list-person-cast-credits?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tVMazeSchedule/latest/actions/list-person-cast-credits?${params}`, {
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
| `embed` | string | no | Optional embedded resource name, such as show or character. |

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
| `_embedded` | object | Optional embedded resources. |
| `_links` | object | Links to show and character. |
| `self` | boolean | Whether the person appears as themself. |
| `voice` | boolean | Whether this is a voice role. |

## Native endpoint

Through the native TVMaze Schedule API, this operation is `GET /people/{{id}}/castcredits` (base URL `https://api.tvmaze.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-person-cast-credits.md) for the provider-specific parameters and requirements.

