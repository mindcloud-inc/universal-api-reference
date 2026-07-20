# Stiply: Download Signer Attachment

Downloads a signer attachment from a Stiply sign request.

```
GET https://connect.mindcloud.co/v1/universal/stiply/latest/actions/download-signer-attachment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stiply `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stiply/latest/actions/download-signer-attachment?connectionId=$CONNECTION_ID&signRequest=1&signerAttachment=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "signRequest": "1",
  "signerAttachment": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stiply/latest/actions/download-signer-attachment?${params}`, {
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
| `signRequest` | number | yes | Id of the signrequest. |
| `signerAttachment` | number | yes | Id of the signer attachment. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Stiply API returns.

## Native endpoint

Through the native Stiply API, this operation is `GET /v2/sign_requests/:sign_request/signer_attachments/:signer_attachment/actions/download_file` (base URL `https://api.stiply.nl`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-signer-attachment.md) for the provider-specific parameters and requirements.

