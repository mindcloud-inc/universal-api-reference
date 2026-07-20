# SigningHub: Download Attachment

Downloads an attachment from SigningHub.

```
GET https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/download-attachment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SigningHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/download-attachment?connectionId=$CONNECTION_ID&attachmentId=1&documentId=1&packageId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "attachmentId": "1",
  "documentId": "1",
  "packageId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/download-attachment?${params}`, {
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
| `attachmentId` | number | yes | ID of the attachment to download. |
| `documentId` | number | yes | Document ID of the document whose attachment is downloaded. |
| `packageId` | number | yes | Package ID of the package to which the document belongs. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | string |  |

## Native endpoint

Through the native SigningHub API, this operation is `GET /v4/packages/:packageId/documents/:documentId/attachments/:attachment_id` (base URL `https://api.signinghub.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-attachment.md) for the provider-specific parameters and requirements.

