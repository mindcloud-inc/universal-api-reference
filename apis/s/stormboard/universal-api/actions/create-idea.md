# Stormboard: Create Idea

Creates an idea in Stormboard.

```
POST https://connect.mindcloud.co/v1/universal/stormboard/latest/actions/create-idea
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stormboard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/stormboard/latest/actions/create-idea" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data": "string",
  "stormId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/stormboard/latest/actions/create-idea', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data": "string",
    "stormId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `color` | string | no | Idea color. |
| `data` | string | yes | Idea content, media URL, or base64 file data depending on the idea type. |
| `ideaType` | string | no | Idea type: text, indexcard, image, video, document, or whiteboard. |
| `lock` | number | no | Set to 1 to lock the idea, or 0 to leave it unlocked. |
| `name` | string | no | Name for a video, whiteboard, image, or document idea. |
| `sectionIndex` | string | no | Place the idea inside a section by index. |
| `shape` | string | no | Idea shape. |
| `stormId` | number | yes | Storm ID where the new idea should be created. |
| `x` | number | no | X position for the new idea. |
| `y` | number | no | Y position for the new idea. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "message": "string",
      "status": 1,
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `message` | string |  |
| `status` | number |  |
| `uuid` | string |  |

## Native endpoint

Through the native Stormboard API, this operation is `POST /ideas` (base URL `https://api.stormboard.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-idea.md) for the provider-specific parameters and requirements.

