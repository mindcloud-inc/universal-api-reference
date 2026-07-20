# Claid AI: Upload Image For Edit

Creates an edited image in Claid AI from upload.

```
POST https://connect.mindcloud.co/v1/universal/claidAI/latest/actions/upload-image-for-edit
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Claid AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/claidAI/latest/actions/upload-image-for-edit" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data": "string",
  "file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/claidAI/latest/actions/upload-image-for-edit', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data": "string",
    "file": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data` | string | yes | JSON string containing the operations and optional output payload for the upload request. |
| `file` | file | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "input": {},
      "output": {},
      "profiling": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `input` | object | Input image metadata. |
| `output` | object | Processed image metadata. |
| `profiling` | object | Execution profiling details. |

## Native endpoint

Through the native Claid AI API, this operation is `POST image/edit/upload` (base URL `https://api.claid.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-image-for-edit.md) for the provider-specific parameters and requirements.

