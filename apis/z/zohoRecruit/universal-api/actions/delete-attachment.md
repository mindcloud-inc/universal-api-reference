# Zoho Recruit: Delete Attachment

Deletes an attachment from a Zoho Recruit record.

```
DELETE https://connect.mindcloud.co/v1/universal/zohoRecruit/latest/actions/delete-attachment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Recruit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/zohoRecruit/latest/actions/delete-attachment?connectionId=$CONNECTION_ID&moduleApiName=Ava%20Chen&recordId=string&attachmentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "moduleApiName": "Ava Chen",
  "recordId": "string",
  "attachmentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoRecruit/latest/actions/delete-attachment?${params}`, {
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
| `moduleApiName` | string | yes | The Zoho Recruit module API name that contains the record. |
| `recordId` | string | yes | The unique ID of the Zoho Recruit record. |
| `attachmentId` | string | yes | The unique ID of the attachment. |

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

Through the native Zoho Recruit API, this operation is `DELETE /:moduleApiName/:recordId/Attachments/:attachmentId` (base URL `https://recruit.zoho.com/recruit/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-attachment.md) for the provider-specific parameters and requirements.

