# Stiply: Download Signer Attachments

Downloads all attachments uploaded by a Stiply signer.

```
GET https://connect.mindcloud.co/v1/universal/stiply/latest/actions/download-signer-attachments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stiply `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stiply/latest/actions/download-signer-attachments?connectionId=$CONNECTION_ID&signRequest=1&signer=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "signRequest": "1",
  "signer": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stiply/latest/actions/download-signer-attachments?${params}`, {
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
| `signer` | number | yes | Id of the signer. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Stiply API returns.

## Native endpoint

Through the native Stiply API, this operation is `GET /v2/sign_requests/:sign_request/signers/:signer/actions/download_signer_attachments` (base URL `https://api.stiply.nl`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-signer-attachments.md) for the provider-specific parameters and requirements.

