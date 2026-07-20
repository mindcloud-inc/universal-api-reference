# Docsumo: Upload Case

Creates or updates a Docsumo case and uploads files.

```
POST https://connect.mindcloud.co/v1/universal/docsumo/latest/actions/upload-case
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Docsumo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/docsumo/latest/actions/upload-case" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "casetype_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docsumo/latest/actions/upload-case', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "casetype_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `casetype_id` | string | yes | Case type identifier to upload into. |
| `file` | string | no | Binary file payload for multipart upload. |
| `file_base64` | string | no | Base64-encoded file content for case upload. |
| `file_url` | string | no | Public URL of the file to upload into the case. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "error": "string",
      "error_code": "string",
      "message": "string",
      "source": "string",
      "status": "string",
      "status_code": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `error` | string |  |
| `error_code` | string |  |
| `message` | string |  |
| `source` | string |  |
| `status` | string |  |
| `status_code` | number |  |

## Native endpoint

Through the native Docsumo API, this operation is `POST /api/v1/upload-service/agents/casetype/case` (base URL `https://app.docsumo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-case.md) for the provider-specific parameters and requirements.

