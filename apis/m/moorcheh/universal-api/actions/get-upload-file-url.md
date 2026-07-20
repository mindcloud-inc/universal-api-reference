# Moorcheh: Get Upload File URL

Generates a pre-signed file upload URL in Moorcheh.

```
POST https://connect.mindcloud.co/v1/universal/moorcheh/latest/actions/get-upload-file-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moorcheh `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/moorcheh/latest/actions/get-upload-file-url" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "namespace_name": "Ava Chen",
  "file_name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moorcheh/latest/actions/get-upload-file-url', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "namespace_name": "Ava Chen",
    "file_name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `namespace_name` | string | yes | Name of the text namespace to upload the file into. |
| `file_name` | string | yes | Target filename including extension, such as document.pdf. Moorcheh auto-detects the content type. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content_type": "string",
      "expires_in": 1,
      "file_name": "Ava Chen",
      "hint": "string",
      "key": "string",
      "method": "string",
      "original_file_name": "Ava Chen",
      "renamed": true,
      "upload_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content_type` | string | Content-Type header to use when uploading. |
| `expires_in` | number | URL expiration time in seconds. |
| `file_name` | string | Final file name used by Moorcheh. |
| `hint` | string | Human-readable upload instructions. |
| `key` | string | S3 object key where the file will be stored. |
| `method` | string | HTTP method to use for upload. |
| `original_file_name` | string | Original requested file name. |
| `renamed` | boolean | Whether Moorcheh renamed the file. |
| `upload_url` | string | Pre-signed S3 URL for uploading the file with PUT. |

## Native endpoint

Through the native Moorcheh API, this operation is `POST /namespaces/:namespace_name/upload-url` (base URL `https://api.moorcheh.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-upload-file-url.md) for the provider-specific parameters and requirements.

