# Fish Audio: Get Model

Finds a voice model in Fish Audio by ID.

```
GET https://connect.mindcloud.co/v1/universal/fishAudio/latest/actions/get-model
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fish Audio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fishAudio/latest/actions/get-model?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fishAudio/latest/actions/get-model?${params}`, {
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
| `id` | string | yes | The Fish Audio model ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "author": {},
      "cover_image": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "languages": [
        "string"
      ],
      "like_count": 1,
      "liked": true,
      "lock_visibility": true,
      "mark_count": 1,
      "marked": true,
      "samples": [
        {}
      ],
      "shared_count": 1,
      "state": "string",
      "tags": [
        "string"
      ],
      "task_count": 1,
      "title": "string",
      "train_mode": "string",
      "type": "string",
      "unliked": true,
      "updated_at": "2026-05-07T12:00:00.000Z",
      "visibility": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string |  |
| `author` | object |  |
| `cover_image` | string |  |
| `created_at` | date |  |
| `description` | string |  |
| `languages` | array<string> |  |
| `like_count` | number |  |
| `liked` | boolean |  |
| `lock_visibility` | boolean |  |
| `mark_count` | number |  |
| `marked` | boolean |  |
| `samples` | array<object> |  |
| `shared_count` | number |  |
| `state` | string |  |
| `tags` | array<string> |  |
| `task_count` | number |  |
| `title` | string |  |
| `train_mode` | string |  |
| `type` | string |  |
| `unliked` | boolean |  |
| `updated_at` | date |  |
| `visibility` | string |  |

## Native endpoint

Through the native Fish Audio API, this operation is `GET /model/:id` (base URL `https://api.fish.audio`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-model.md) for the provider-specific parameters and requirements.

