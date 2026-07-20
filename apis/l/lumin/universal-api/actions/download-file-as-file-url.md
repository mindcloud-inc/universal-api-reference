# Lumin: Download File As File URL



```
GET https://connect.mindcloud.co/v1/universal/lumin/latest/actions/download-file-as-file-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lumin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lumin/latest/actions/download-file-as-file-url?connectionId=$CONNECTION_ID&signatureRequestId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "signatureRequestId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lumin/latest/actions/download-file-as-file-url?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `signatureRequestId` | string | yes | ID of the signature request. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "expiresAt": 1,
      "fileUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `expiresAt` | number |  |
| `fileUrl` | string |  |

## Native endpoint

Through the native Lumin API, this operation is `GET /signature_request/files_as_file_url/:signature_request_id` (base URL `https://api.luminpdf.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-file-as-file-url.md) for the provider-specific parameters and requirements.

