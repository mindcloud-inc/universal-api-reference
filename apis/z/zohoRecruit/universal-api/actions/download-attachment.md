# Zoho Recruit: Download Attachment

Retrieves an attachment from a Zoho Recruit record.

```
GET https://connect.mindcloud.co/v1/universal/zohoRecruit/latest/actions/download-attachment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Recruit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoRecruit/latest/actions/download-attachment?connectionId=$CONNECTION_ID&moduleApiName=Ava%20Chen&recordId=string&attachmentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "moduleApiName": "Ava Chen",
  "recordId": "string",
  "attachmentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoRecruit/latest/actions/download-attachment?${params}`, {
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

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Zoho Recruit API returns.

## Native endpoint

Through the native Zoho Recruit API, this operation is `GET /:moduleApiName/:recordId/Attachments/:attachmentId` (base URL `https://recruit.zoho.com/recruit/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-attachment.md) for the provider-specific parameters and requirements.

