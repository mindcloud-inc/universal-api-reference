# Dropbox Sign: Cancel Signature Request

Cancels a signature request in Dropbox Sign.

```
DELETE https://connect.mindcloud.co/v1/universal/dropboxSign/latest/actions/cancel-signature-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dropbox Sign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/dropboxSign/latest/actions/cancel-signature-request?connectionId=$CONNECTION_ID&signature_request_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "signature_request_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dropboxSign/latest/actions/cancel-signature-request?${params}`, {
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
| `signature_request_id` | string | yes | The id of the incomplete SignatureRequest to cancel. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Dropbox Sign API returns.

## Native endpoint

Through the native Dropbox Sign API, this operation is `POST /signature_request/cancel/:signature_request_id` (base URL `https://api.hellosign.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-signature-request.md) for the provider-specific parameters and requirements.

