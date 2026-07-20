# Zoho Mail: Download Attachment

Retrieves attachment content from Zoho Mail.

```
GET https://connect.mindcloud.co/v1/universal/zohoMail/latest/actions/download-attachment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Mail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoMail/latest/actions/download-attachment?connectionId=$CONNECTION_ID&accountId=string&folderId=3048445000000008014&messageId=1773241114744157000&attachmentId=3048445000000009001" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "string",
  "folderId": "3048445000000008014",
  "messageId": "1773241114744157000",
  "attachmentId": "3048445000000009001"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoMail/latest/actions/download-attachment?${params}`, {
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
| `accountId` | list<string> | yes | Zoho Mail account ID. |
| `folderId` | string | yes | Folder ID containing the email. Example: `3048445000000008014`. |
| `messageId` | string | yes | Message ID of the email. Example: `1773241114744157000`. |
| `attachmentId` | string | yes | Attachment ID to download. Example: `3048445000000009001`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        1
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<number> | Attachment byte values returned from Zoho Mail. |
| `type` | string | Raw binary payload wrapper type from the runtime response. |

## Native endpoint

Through the native Zoho Mail API, this operation is `GET /accounts/:accountId/folders/:folderId/messages/:messageId/attachments/:attachmentId` (base URL `https://mail.zoho.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-attachment.md) for the provider-specific parameters and requirements.

