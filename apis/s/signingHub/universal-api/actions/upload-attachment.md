# SigningHub: Upload Attachment

Uploads an attachment to SigningHub.

```
POST https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/upload-attachment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SigningHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/upload-attachment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "packageId": "11191528",
  "documentId": "13459082",
  "file": "Raw binary attachment content"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/upload-attachment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "packageId": "11191528",
    "documentId": "13459082",
    "file": "Raw binary attachment content"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `packageId` | number | yes | Package ID of the package to which the document is added. Example: `11191528`. |
| `documentId` | number | yes | ID of the document to which the attachment needs to be added. Example: `13459082`. |
| `file` | string | yes | Raw binary attachment content to upload. Example: `Raw binary attachment content`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attachment_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attachment_id` | number |  |

## Native endpoint

Through the native SigningHub API, this operation is `POST /v4/packages/:packageId/documents/:documentId/attachments` (base URL `https://api.signinghub.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-attachment.md) for the provider-specific parameters and requirements.

