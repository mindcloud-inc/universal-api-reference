# SigningHub: Delete Attachment

Deletes an attachment from SigningHub.

```
DELETE https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/delete-attachment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SigningHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/delete-attachment?connectionId=$CONNECTION_ID&packageId=1&documentId=1&attachmentId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "packageId": "1",
  "documentId": "1",
  "attachmentId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/delete-attachment?${params}`, {
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
| `packageId` | number | yes | The document package containing the attachment to delete. |
| `documentId` | number | yes | The document containing the attachment to delete. |
| `attachmentId` | number | yes | The attachment to delete. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SigningHub API returns.

## Native endpoint

Through the native SigningHub API, this operation is `DELETE /v4/packages/:packageId/documents/:documentId/attachments/:attachmentId` (base URL `https://api.signinghub.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-attachment.md) for the provider-specific parameters and requirements.

