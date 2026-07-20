# Skribble Sign: Remove Signature Request Attachment

Deletes a signature request attachment from Skribble Sign.

```
DELETE https://connect.mindcloud.co/v1/universal/skribbleSign/latest/actions/remove-signature-request-attachment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Skribble Sign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/skribbleSign/latest/actions/remove-signature-request-attachment?connectionId=$CONNECTION_ID&signatureRequestId=string&attachmentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "signatureRequestId": "string",
  "attachmentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/skribbleSign/latest/actions/remove-signature-request-attachment?${params}`, {
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
| `signatureRequestId` | string | yes | The signature request ID. |
| `attachmentId` | string | yes | The attachment ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | Whether the attachment was removed. |

## Native endpoint

Through the native Skribble Sign API, this operation is `DELETE /v2/signature-requests/:signatureRequestId/attachments/:attachmentId` (base URL `https://api.skribble.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-signature-request-attachment.md) for the provider-specific parameters and requirements.

