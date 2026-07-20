# Open AI: Upload File

Uploads a file to Open AI.

```
POST https://connect.mindcloud.co/v1/universal/openAi/latest/actions/upload-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Open AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/openAi/latest/actions/upload-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string",
  "purpose": "assistants"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/openAi/latest/actions/upload-file', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "string",
    "purpose": "assistants"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file` | file | yes | File content or file source to upload. |
| `purpose` | list | yes | Intended purpose of the uploaded file. Default: `assistants`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bytes": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "expiresAt": "2026-05-07T12:00:00.000Z",
      "filename": "Ava Chen",
      "id": "string",
      "object": "string",
      "purpose": "string",
      "status": "string",
      "statusDetails": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bytes` | number |  |
| `createdAt` | date |  |
| `expiresAt` | date |  |
| `filename` | string |  |
| `id` | string |  |
| `object` | string |  |
| `purpose` | string |  |
| `status` | string |  |
| `statusDetails` | date |  |

## Native endpoint

Through the native Open AI API, this operation is `POST v1/files` (base URL `https://api.openai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-file.md) for the provider-specific parameters and requirements.

