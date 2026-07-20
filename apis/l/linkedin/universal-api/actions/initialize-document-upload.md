# LinkedIn: Initialize Document Upload

Initializes a document upload in LinkedIn.

```
POST https://connect.mindcloud.co/v1/universal/linkedin/latest/actions/initialize-document-upload
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LinkedIn `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/linkedin/latest/actions/initialize-document-upload" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "initializeUploadRequest.owner": "urn:li:person:vdyhqnicOV"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/linkedin/latest/actions/initialize-document-upload', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "initializeUploadRequest.owner": "urn:li:person:vdyhqnicOV"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `initializeUploadRequest.owner` | string | yes | Owner URN for the member initializing the upload. Example: `urn:li:person:vdyhqnicOV`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": {
        "document": "string",
        "uploadUrl": "https://example.com",
        "uploadUrlExpiresAt": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | object |  |
| `value.document` | string |  |
| `value.uploadUrl` | string |  |
| `value.uploadUrlExpiresAt` | number |  |

## Native endpoint

Through the native LinkedIn API, this operation is `POST /rest/documents?action=initializeUpload` (base URL `https://api.linkedin.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/initialize-document-upload.md) for the provider-specific parameters and requirements.

