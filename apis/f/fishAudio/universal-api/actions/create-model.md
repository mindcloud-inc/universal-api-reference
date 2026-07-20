# Fish Audio: Create Model

Creates a new voice model in Fish Audio.

```
POST https://connect.mindcloud.co/v1/universal/fishAudio/latest/actions/create-model
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fish Audio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fishAudio/latest/actions/create-model" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string",
  "voices[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fishAudio/latest/actions/create-model', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string",
    "voices[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `visibility` | list | no | Whether the model is public, unlisted, or private. One of: `0`, `1`, `2`. Default: `public`. |
| `title` | string | yes | Model title or name. |
| `description` | string | no | Model description. |
| `coverImage` | file | no | Optional cover image. Required by Fish Audio when visibility is public. |
| `voices[]` | array<file> | yes | One or more voice audio files used to create the model. |
| `texts[]` | array<string> | no | Optional transcripts aligned to the uploaded voice files. |
| `tags[]` | array<string> | no | Optional model tags. |
| `enhanceAudioQuality` | boolean | no | When true, Fish Audio enhances uploaded audio quality. Default: `false`. |

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

Through the native Fish Audio API, this operation is `POST /model` (base URL `https://api.fish.audio`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-model.md) for the provider-specific parameters and requirements.

