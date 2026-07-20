# Manus: Create File

Creates a file in Manus and returns a presigned upload URL.

```
POST https://connect.mindcloud.co/v1/universal/manus/latest/actions/create-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Manus `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/manus/latest/actions/create-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "filename": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/manus/latest/actions/create-file', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "filename": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filename` | string | yes | Name of the file to upload |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "filename": "Ava Chen",
      "id": "string",
      "object": "string",
      "status": "string",
      "uploadExpiresAt": "string",
      "uploadUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `filename` | string |  |
| `id` | string |  |
| `object` | string |  |
| `status` | string |  |
| `uploadExpiresAt` | string |  |
| `uploadUrl` | string |  |

## Native endpoint

Through the native Manus API, this operation is `POST /files` (base URL `https://api.manus.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-file.md) for the provider-specific parameters and requirements.

