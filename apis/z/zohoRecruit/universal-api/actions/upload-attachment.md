# Zoho Recruit: Upload Attachment

Uploads an attachment to a Zoho Recruit record.

```
POST https://connect.mindcloud.co/v1/universal/zohoRecruit/latest/actions/upload-attachment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Recruit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoRecruit/latest/actions/upload-attachment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "moduleApiName": "Ava Chen",
  "recordId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoRecruit/latest/actions/upload-attachment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "moduleApiName": "Ava Chen",
    "recordId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `moduleApiName` | string | yes | The Zoho Recruit module API name that contains the record. |
| `recordId` | string | yes | The unique ID of the Zoho Recruit record. |
| `file` | file | no | The file to attach to the record. |
| `attachmentsCategory` | string | no | Attachment category labels for the uploaded file. Accepts multiple values in one string, delimited by `,`. |
| `attachmentsCategoryId` | string | no | Attachment category IDs for the uploaded file. Accepts multiple values in one string, delimited by `,`. |
| `attachmentUrl` | string | no | A publicly reachable file URL for the attachment when you are not uploading a binary file directly. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "details": {},
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string |  |
| `details` | object |  |
| `message` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Zoho Recruit API, this operation is `POST /:moduleApiName/:recordId/Attachments` (base URL `https://recruit.zoho.com/recruit/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-attachment.md) for the provider-specific parameters and requirements.

