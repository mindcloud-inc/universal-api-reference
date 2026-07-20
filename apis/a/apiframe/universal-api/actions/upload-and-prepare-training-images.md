# Apiframe: Upload and Prepare Training Images

Uploads and prepares AI photo training images in Apiframe.

```
POST https://connect.mindcloud.co/v1/universal/apiframe/latest/actions/upload-and-prepare-training-images
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Apiframe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/apiframe/latest/actions/upload-and-prepare-training-images" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "images[]": [
    "string"
  ],
  "ethnicity": "string",
  "gender": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/apiframe/latest/actions/upload-and-prepare-training-images', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "images[]": ["string"],
    "ethnicity": "string",
    "gender": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `images[]` | array<string> | yes |  |
| `ethnicity` | string | yes |  |
| `gender` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "task_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `task_id` | string |  |

## Native endpoint

Through the native Apiframe API, this operation is `POST /ai-photo-upload` (base URL `https://api.apiframe.pro`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-and-prepare-training-images.md) for the provider-specific parameters and requirements.

