# JoggAI: Create Photo Avatar



```
POST https://connect.mindcloud.co/v1/universal/joggAI/latest/actions/create-photo-avatar
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a JoggAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/joggAI/latest/actions/create-photo-avatar" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "age": "string",
  "avatarStyle": "string",
  "gender": "string",
  "model": "string",
  "aspectRatio": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/joggAI/latest/actions/create-photo-avatar', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "age": "string",
    "avatarStyle": "string",
    "gender": "string",
    "model": "string",
    "aspectRatio": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `age` | string | yes |  |
| `avatarStyle` | string | yes |  |
| `gender` | string | yes |  |
| `model` | string | yes |  |
| `aspectRatio` | string | yes |  |
| `ethnicity` | string | no |  |
| `background` | string | no |  |
| `appearance` | string | no |  |
| `imageUrl` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "photoId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `photoId` | string | Generated photo avatar request ID |

## Native endpoint

Through the native JoggAI API, this operation is `POST /v2/photo_avatar/photo/generate` (base URL `https://api.jogg.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-photo-avatar.md) for the provider-specific parameters and requirements.

