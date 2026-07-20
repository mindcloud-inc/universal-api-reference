# Zoho Mail: Get Email Metadata

Retrieves email metadata from Zoho Mail.

```
GET https://connect.mindcloud.co/v1/universal/zohoMail/latest/actions/get-email-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Mail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoMail/latest/actions/get-email-metadata?connectionId=$CONNECTION_ID&accountId=string&folderId=3048445000000008014&messageId=1773241114744157000" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "string",
  "folderId": "3048445000000008014",
  "messageId": "1773241114744157000"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoMail/latest/actions/get-email-metadata?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "calendarType": 1,
      "ccAddress": "string",
      "flagid": "string",
      "folderId": "string",
      "fromAddress": "string",
      "hasAttachment": "string",
      "hasInline": "string",
      "labelId": [
        "string"
      ],
      "messageId": "string",
      "priority": "string",
      "receivedTime": "string",
      "sender": "string",
      "sentDateInGMT": "string",
      "size": "string",
      "status": "string",
      "status2": "string",
      "subject": "string",
      "summary": "string",
      "toAddress": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `calendarType` | number | Calendar type |
| `ccAddress` | string | CC address |
| `flagid` | string | Flag identifier |
| `folderId` | string | Folder identifier |
| `fromAddress` | string | From address |
| `hasAttachment` | string | Attachment flag |
| `hasInline` | string | Inline content flag |
| `labelId` | array<string> | Applied label identifiers |
| `messageId` | string | Message identifier |
| `priority` | string | Priority code |
| `receivedTime` | string | Received timestamp |
| `sender` | string | Sender |
| `sentDateInGMT` | string | Sent date timestamp in GMT |
| `size` | string | Message size |
| `status` | string | Read status code |
| `status2` | string | Secondary status code |
| `subject` | string | Email subject |
| `summary` | string | Email summary |
| `toAddress` | string | To address |

## Native endpoint

Through the native Zoho Mail API, this operation is `GET /accounts/:accountId/folders/:folderId/messages/:messageId/details` (base URL `https://mail.zoho.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-email-metadata.md) for the provider-specific parameters and requirements.

