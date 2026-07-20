# PiAPI/Trellis: Create Trellis Image-to-3D Task

Creates a Trellis image-to-3D task in PiAPI/Trellis.

```
POST https://connect.mindcloud.co/v1/universal/piAPITrellis/latest/actions/create-trellis-image-to-3d-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PiAPI/Trellis `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/piAPITrellis/latest/actions/create-trellis-image-to-3d-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "input.images[]": "https://upload.wikimedia.org/wikipedia/commons/3/3a/Cat03.jpg"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/piAPITrellis/latest/actions/create-trellis-image-to-3d-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "input.images[]": "https://upload.wikimedia.org/wikipedia/commons/3/3a/Cat03.jpg"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `input.prompt` | string | no | Prompt describing the desired 3D object. Example: `a toy robot`. |
| `input.images[]` | array<string> | yes | One or more source image URLs. Accepts multiple values as an array. Example: `https://upload.wikimedia.org/wikipedia/commons/3/3a/Cat03.jpg`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native PiAPI/Trellis API returns.

## Native endpoint

Through the native PiAPI/Trellis API, this operation is `POST /api/v1/task` (base URL `https://api.piapi.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-trellis-image-to-3d-task.md) for the provider-specific parameters and requirements.

