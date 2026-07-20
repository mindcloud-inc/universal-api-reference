# Zoho Mail: Search Emails

Finds emails in Zoho Mail by search parameters.

```
GET https://connect.mindcloud.co/v1/universal/zohoMail/latest/actions/search-emails
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Mail `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoMail/latest/actions/search-emails?connectionId=$CONNECTION_ID&limit=25&offset=0&accountId=string&searchKey=from%3Awelcome%40zoho.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "accountId": "string",
  "searchKey": "from:welcome@zoho.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoMail/latest/actions/search-emails?${params}`, {
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
| `searchKey` | string | yes | Search criteria string in Zoho Mail search syntax, for example from:welcome@zoho.com or has:attachment. Example: `from:welcome@zoho.com`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `receivedTime` | number | no | Limit search to emails received within the given number of days. Example: `30`. |
| `includeTo` | boolean | no | Whether recipient fields should be included in the search scope. |

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
      "mailDeliveryStatus": "string",
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
      "toAddr": "string",
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
| `mailDeliveryStatus` | string | Delivery status |
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
| `toAddr` | string | To address summary |
| `toAddress` | string | To address |

## Native endpoint

Through the native Zoho Mail API, this operation is `GET /accounts/:accountId/messages/search` (base URL `https://mail.zoho.com/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-emails.md) for the provider-specific parameters and requirements.

