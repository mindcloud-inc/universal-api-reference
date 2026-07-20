# TVMaze Schedule: List Show Images

Retrieves images for a TVMaze show.

```
GET https://connect.mindcloud.co/v1/universal/tVMazeSchedule/latest/actions/list-show-images
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TVMaze Schedule `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tVMazeSchedule/latest/actions/list-show-images?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tVMazeSchedule/latest/actions/list-show-images?${params}`, {
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
| `id` | number | yes | Required TVmaze show ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "main": true,
      "resolutions": {},
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number | Image ID. |
| `main` | boolean | Whether this is the primary image. |
| `resolutions` | object | Available image resolutions. |
| `type` | string | Image type. |

## Native endpoint

Through the native TVMaze Schedule API, this operation is `GET /shows/{{id}}/images` (base URL `https://api.tvmaze.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-show-images.md) for the provider-specific parameters and requirements.

