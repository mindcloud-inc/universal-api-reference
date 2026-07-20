# Skribble: Remove Signature Request Attachment

Removes an attachment from a signature request in Skribble.

```
DELETE https://connect.mindcloud.co/v1/universal/skribble/latest/actions/remove-signature-request-attachment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Skribble `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/skribble/latest/actions/remove-signature-request-attachment?connectionId=$CONNECTION_ID&attachmentId=string&signatureRequestId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "attachmentId": "string",
  "signatureRequestId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/skribble/latest/actions/remove-signature-request-attachment?${params}`, {
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
| `attachmentId` | string | yes | The attachment ID. |
| `signatureRequestId` | string | yes | The signature request ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Skribble API returns.

## Native endpoint

Through the native Skribble API, this operation is `DELETE /v2/signature-requests/:signatureRequestId/attachments/:attachmentId` (base URL `https://api.skribble.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-signature-request-attachment.md) for the provider-specific parameters and requirements.

