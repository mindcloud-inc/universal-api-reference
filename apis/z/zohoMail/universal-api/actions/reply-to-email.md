# Zoho Mail: Reply To Email

Replies to an email in Zoho Mail.

```
POST https://connect.mindcloud.co/v1/universal/zohoMail/latest/actions/reply-to-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Mail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoMail/latest/actions/reply-to-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": "string",
  "messageId": "1223334444444",
  "fromAddress": "me@example.com",
  "toAddress": "recipient@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoMail/latest/actions/reply-to-email', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": "string",
    "messageId": "1223334444444",
    "fromAddress": "me@example.com",
    "toAddress": "recipient@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | list<string> | yes | Zoho Mail account ID to send the reply from. |
| `messageId` | string | yes | Message ID of the email you want to reply to. Example: `1223334444444`. |
| `fromAddress` | string | yes | Sender email address associated with the authenticated Zoho Mail account. Example: `me@example.com`. |
| `toAddress` | string | yes | Recipient email address for the reply. Example: `recipient@example.com`. |
| `content` | string | no | Reply body content. This field is shown in the official sample request. Example: `Thanks for the update.`. |
| `subject` | string | no | Reply subject line. Example: `Re: Quick update`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ccAddress` | string | no | Optional CC recipient email address. Example: `manager@example.com`. |
| `bccAddress` | string | no | Optional BCC recipient email address. Example: `audit@example.com`. |
| `mailFormat` | list<string> | no | Format used to send the reply body. One of: `html`, `plaintext`. |
| `askReceipt` | list<string> | no | Whether to request a read receipt from the recipient. One of: `no`, `yes`. |
| `encoding` | list<string> | no | Character encoding for the reply content. One of: `Big5`, `EUC-JP`, `EUC-KR`, `GB2312`, `ISO-2022-JP`, `ISO-8859-1`, `KOI8-R`, `Shift_JIS`, `US-ASCII`, `UTF-8`, `WINDOWS-1251`, `X-WINDOWS-ISO2022JP`. |
| `isSchedule` | boolean | no | Whether to schedule the reply instead of sending it immediately. |
| `scheduleType` | list<number> | no | Scheduling preset to use when sending the reply later. One of: `1`, `2`, `3`, `4`, `5`, `6`. |
| `timeZone` | string | no | Time zone used for a custom scheduled reply when Schedule Type is 6. Example: `GMT 5:30 (India Standard Time - Asia/Calcutta)`. |
| `scheduleTime` | string | no | Custom date and time for the scheduled reply in MM/DD/YYYY HH:MM:SS format. Example: `09/15/2023 14:30:28`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "action": "string",
      "content": "string",
      "fromAddress": "string",
      "mailId": "string",
      "messageId": "string",
      "toAddress": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `action` | string | Reply action |
| `content` | string | Reply body content |
| `fromAddress` | string | From address |
| `mailId` | string | Mail header identifier |
| `messageId` | string | Message identifier |
| `toAddress` | string | To address |

## Native endpoint

Through the native Zoho Mail API, this operation is `POST /accounts/:accountId/messages/:messageId` (base URL `https://mail.zoho.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/reply-to-email.md) for the provider-specific parameters and requirements.

