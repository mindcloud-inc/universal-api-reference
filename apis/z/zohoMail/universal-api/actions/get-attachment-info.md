# Zoho Mail: Get Attachment Info

Retrieves attachment info from Zoho Mail.

```
GET https://connect.mindcloud.co/v1/universal/zohoMail/latest/actions/get-attachment-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Mail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoMail/latest/actions/get-attachment-info?connectionId=$CONNECTION_ID&accountId=string&folderId=3048445000000008014&messageId=1773241114744157000" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "string",
  "folderId": "3048445000000008014",
  "messageId": "1773241114744157000"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoMail/latest/actions/get-attachment-info?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `includeInline` | boolean | no | Whether inline attachments should be included in the attachment info response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attachments": [
        {}
      ],
      "messageId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attachments` | array<object> | Attachment metadata rows |
| `messageId` | string | Message identifier |

## Native endpoint

Through the native Zoho Mail API, this operation is `GET /accounts/:accountId/folders/:folderId/messages/:messageId/attachmentinfo` (base URL `https://mail.zoho.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-attachment-info.md) for the provider-specific parameters and requirements.

