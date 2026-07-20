# Lumin: Get Signature Request File



```
GET https://connect.mindcloud.co/v1/universal/lumin/latest/actions/get-signature-request-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lumin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lumin/latest/actions/get-signature-request-file?connectionId=$CONNECTION_ID&signatureRequestId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "signatureRequestId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lumin/latest/actions/get-signature-request-file?${params}`, {
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
| `type` | string | no | Artifact to return: agreement, coc, or merged. Default: `agreement`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "expiresAt": 1,
      "signedUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `expiresAt` | number |  |
| `signedUrl` | string |  |

## Native endpoint

Through the native Lumin API, this operation is `GET /signature_request/:signature_request_id/file` (base URL `https://api.luminpdf.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-signature-request-file.md) for the provider-specific parameters and requirements.

