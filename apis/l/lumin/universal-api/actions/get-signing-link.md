# Lumin: Get Signing Link



```
GET https://connect.mindcloud.co/v1/universal/lumin/latest/actions/get-signing-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lumin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lumin/latest/actions/get-signing-link?connectionId=$CONNECTION_ID&signatureRequestId=string&signerEmail=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "signatureRequestId": "string",
  "signerEmail": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lumin/latest/actions/get-signing-link?${params}`, {
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
| `signerEmail` | string | yes | Email address of the signer whose signing link should be generated. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "signerEmail": "ava@example.com",
      "status": "string",
      "viewUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `signerEmail` | string |  |
| `status` | string |  |
| `viewUrl` | string |  |

## Native endpoint

Through the native Lumin API, this operation is `POST /signature_request/:signature_request_id/signing-link` (base URL `https://api.luminpdf.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-signing-link.md) for the provider-specific parameters and requirements.

