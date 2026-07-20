# Runway: Upload File

Creates an ephemeral file upload in Runway.

```
POST https://connect.mindcloud.co/v1/universal/runway/latest/actions/upload-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Runway `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/runway/latest/actions/upload-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "filename": "Ava Chen",
  "type": "ephemeral"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/runway/latest/actions/upload-file', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "filename": "Ava Chen",
    "type": "ephemeral"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filename` | string | yes | Filename with a supported image, video, or audio extension. |
| `type` | string | yes | Upload type. Runway currently requires ephemeral. Default: `ephemeral`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error": "string",
      "id": "string",
      "status": "string",
      "uploadUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error` | string |  |
| `id` | string |  |
| `status` | string |  |
| `uploadUrl` | string |  |

## Native endpoint

Through the native Runway API, this operation is `POST /v1/uploads` (base URL `https://api.dev.runwayml.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-file.md) for the provider-specific parameters and requirements.

