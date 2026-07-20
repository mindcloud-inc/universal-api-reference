# Zoho Mail: List Emails

Retrieves email messages from Zoho Mail.

```
GET https://connect.mindcloud.co/v1/universal/zohoMail/latest/actions/list-emails
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Mail `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoMail/latest/actions/list-emails?connectionId=$CONNECTION_ID&limit=25&offset=0&accountId=3048445000000008002" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "accountId": "3048445000000008002"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoMail/latest/actions/list-emails?${params}`, {
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
| `accountId` | string | yes | Account identifier returned by List Accounts. Example: `3048445000000008002`. |
| `folderId` | string | no | Folder identifier returned by List Folders. Example: `3048445000000008014`. |
| `status` | string | no | Filter emails by read or unread status. Example: `all`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `labelId` | string | no | Filter emails by label identifier. Example: `3048445000000012001`. |
| `threadId` | string | no | Filter emails by thread identifier. |
| `flagId` | number | no | Filter emails by flag type identifier. Example: `1`. |
| `includeTo` | boolean | no | Include recipient details in the response. Example: `true`. |
| `includeSent` | boolean | no | Include sent emails in the response. Example: `true`. |
| `includeArchive` | boolean | no | Include archived emails in the response. Example: `true`. |
| `attachedMails` | boolean | no | Only return emails with attachments when true. Example: `true`. |
| `inlinedMails` | boolean | no | Only return emails with inline images when true. Example: `true`. |
| `flaggedMails` | boolean | no | Only return flagged emails when true. Example: `true`. |
| `respondedMails` | boolean | no | Only return emails with replies when true. Example: `true`. |
| `threadedMails` | boolean | no | Only return threaded emails when true. Example: `true`. |

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

Through the native Zoho Mail API, this operation is `GET /accounts/:accountId/messages/view` (base URL `https://mail.zoho.com/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-emails.md) for the provider-specific parameters and requirements.

