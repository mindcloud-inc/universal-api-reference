# leadtributor.cloud: Announce Lead Attachment Upload

Creates an attachment upload request for a lead in leadtributor.cloud.

```
POST https://connect.mindcloud.co/v1/universal/leadtributorcloud/latest/actions/announce-lead-attachment-upload
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a leadtributor.cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/leadtributorcloud/latest/actions/announce-lead-attachment-upload" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contentType": "string",
  "filename": "Ava Chen",
  "leadId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/leadtributorcloud/latest/actions/announce-lead-attachment-upload', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contentType": "string",
    "filename": "Ava Chen",
    "leadId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contentType` | string | yes | MIME type of the attachment to upload. |
| `filename` | string | yes | Filename to announce for upload. |
| `leadId` | string | yes | ID of the lead to attach a file to. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fields": {},
      "uploadUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fields` | object | Form fields required for the upload request. |
| `uploadUrl` | string | Presigned upload URL for the attachment binary. |

## Native endpoint

Through the native leadtributor.cloud API, this operation is `POST /leads/:leadId/attachments` (base URL `https://api.leadtributor.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/announce-lead-attachment-upload.md) for the provider-specific parameters and requirements.

