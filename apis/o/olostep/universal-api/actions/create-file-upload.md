# Olostep: Create File Upload

Creates a new file upload in Olostep.

```
POST https://connect.mindcloud.co/v1/universal/olostep/latest/actions/create-file-upload
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Olostep `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/olostep/latest/actions/create-file-upload" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "filename": "knowledge-base.json"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/olostep/latest/actions/create-file-upload', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "filename": "knowledge-base.json"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filename` | string | yes | The JSON filename to register before uploading file bytes. Example: `knowledge-base.json`. |
| `purpose` | string | no | Why you are uploading this file. One of: `0`. Example: `context`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "2026-05-07T12:00:00.000Z",
      "expiresIn": 1,
      "id": "string",
      "object": "string",
      "uploadUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date |  |
| `expiresIn` | number |  |
| `id` | string |  |
| `object` | string |  |
| `uploadUrl` | string |  |

## Native endpoint

Through the native Olostep API, this operation is `POST /v1/files` (base URL `https://api.olostep.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-file-upload.md) for the provider-specific parameters and requirements.

