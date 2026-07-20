# ManyReach: List Senders

Retrieves senders from ManyReach.

```
GET https://connect.mindcloud.co/v1/universal/manyReach/latest/actions/list-senders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ManyReach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/manyReach/latest/actions/list-senders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/manyReach/latest/actions/list-senders?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "accountType": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customImapPort": "string",
      "customImapServer": "string",
      "customImapUsername": "Ava Chen",
      "customSmtpPort": 1,
      "customSmtpServer": "string",
      "customSmtpUsername": "Ava Chen",
      "customWarmupTag": "string",
      "dailyLimit": 1,
      "dailyLimitIncrease": true,
      "dailyLimitIncreasePercent": 1,
      "dailyLimitIncreaseToMax": 1,
      "dateDisconnected": "2026-05-07T12:00:00.000Z",
      "dateWarmupDisconnected": "2026-05-07T12:00:00.000Z",
      "delayMin": 1,
      "disconnected": true,
      "disconnectionReason": "string",
      "email": "ava@example.com",
      "firstName": "Ava",
      "folder": "string",
      "fromName": "Ava Chen",
      "lastName": "Chen",
      "replyTo": "string",
      "senderCustom1": "string",
      "senderCustom10": "string",
      "senderCustom2": "string",
      "senderCustom3": "string",
      "senderCustom4": "string",
      "senderCustom5": "string",
      "senderCustom6": "string",
      "senderCustom7": "string",
      "senderCustom8": "string",
      "senderCustom9": "string",
      "senderId": 1,
      "signature": "string",
      "trackingDomain": "string",
      "warmup": true,
      "warmupDailyLimit": 1,
      "warmupDailyLimitIncrease": true,
      "warmupDailyLimitIncreasePercent": 1,
      "warmupDailyLimitIncreaseToMax": 1,
      "warmupRemovalReason": "string",
      "warmupReplyPercent": 1,
      "warmupSkipWeekends": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountType` | string | Type of sender account: customsmtp, gmailsmtp, gmailoauth, msoauth, sendgridapi |
| `createdAt` | date | Timestamp when the sender account was created in the system. |
| `customImapPort` | string | IMAP server port number for custom email retrieval configuration; typically 993 for SSL/TLS; maximum 64 characters. |
| `customImapServer` | string | IMAP server hostname for custom email retrieval configuration; maximum 128 characters. |
| `customImapUsername` | string | Custom IMAP username if different from the sender email; maximum 128 characters. |
| `customSmtpPort` | number | SMTP server port number for custom email sending configuration. |
| `customSmtpServer` | string | SMTP server hostname for custom email sending configuration; maximum 128 characters. |
| `customSmtpUsername` | string | Custom SMTP username if different from the sender email; maximum 128 characters. |
| `customWarmupTag` | string | Custom tag applied to emails sent during warmup phase for tracking and filtering purposes; maximum 64 characters. |
| `dailyLimit` | number | Maximum number of emails this sender can send per day; must be between 1 and 10,000. |
| `dailyLimitIncrease` | boolean | Enable automatic progressive increase of the daily sending limit to scale up sending capacity over time. |
| `dailyLimitIncreasePercent` | number | Daily percentage increase applied to the sending limit when progressive increase is enabled; must be between 1 and 100. |
| `dailyLimitIncreaseToMax` | number | Target maximum daily sending limit when using progressive increase; must be greater than current daily limit. |
| `dateDisconnected` | date | Timestamp when the sender account was disconnected from the email provider. |
| `dateWarmupDisconnected` | date | Timestamp when the sender was removed from the public warmup network. |
| `delayMin` | number | Minimum delay in seconds between sending consecutive emails from this sender to avoid triggering spam filters; default 120 seconds. |
| `disconnected` | boolean | Indicates whether the sender account is currently disconnected from the email provider due to authentication or connection issues. |
| `disconnectionReason` | string | Reason why the sender account was disconnected; maximum 128 characters. |
| `email` | string | Email address of the sender account used for outgoing campaigns; must be valid email format with maximum 100 characters. |
| `firstName` | string | Sender's first name used for personalization in campaigns; maximum 128 characters. |
| `folder` | string | Organizational folder name for grouping and categorizing sender accounts; maximum 64 characters. |
| `fromName` | string | Display name shown as the sender in outgoing emails; maximum 128 characters. |
| `lastName` | string | Sender's last name used for personalization in campaigns; maximum 128 characters. |
| `replyTo` | string | Reply-to email address for responses to campaigns; must be valid email format, maximum 128 characters. If set, Unibox will not catch replies unless Reply-to sender is also connected as sender. |
| `senderCustom1` | string | Custom field 1 for storing additional sender-specific data; maximum 4,000 characters. |
| `senderCustom10` | string | Custom field 10 for storing additional sender-specific data; maximum 4,000 characters. |
| `senderCustom2` | string | Custom field 2 for storing additional sender-specific data; maximum 4,000 characters. |
| `senderCustom3` | string | Custom field 3 for storing additional sender-specific data; maximum 4,000 characters. |
| `senderCustom4` | string | Custom field 4 for storing additional sender-specific data; maximum 4,000 characters. |
| `senderCustom5` | string | Custom field 5 for storing additional sender-specific data; maximum 4,000 characters. |
| `senderCustom6` | string | Custom field 6 for storing additional sender-specific data; maximum 4,000 characters. |
| `senderCustom7` | string | Custom field 7 for storing additional sender-specific data; maximum 4,000 characters. |
| `senderCustom8` | string | Custom field 8 for storing additional sender-specific data; maximum 4,000 characters. |
| `senderCustom9` | string | Custom field 9 for storing additional sender-specific data; maximum 4,000 characters. |
| `senderId` | number | Unique identifier for the sender account. |
| `signature` | string | Email signature HTML content appended to the bottom of outgoing messages. |
| `trackingDomain` | string | Custom domain used for tracking links and open tracking in emails; maximum 256 characters. |
| `warmup` | boolean | Enable warmup to gradually build sender reputation. |
| `warmupDailyLimit` | number | Initial daily sending limit when starting the warmup process; default 10 emails per day. |
| `warmupDailyLimitIncrease` | boolean | Enable progressive daily limit increase specifically during the warmup period to gradually build sender reputation. |
| `warmupDailyLimitIncreasePercent` | number | Daily percentage increase of the sending limit during warmup period; must be between 1 and 10,000. |
| `warmupDailyLimitIncreaseToMax` | number | Target maximum daily sending limit to reach during the warmup phase; must be between 1 and 10,000. |
| `warmupRemovalReason` | string | Reason why the sender was removed from the public warmup network; maximum 128 characters. |
| `warmupReplyPercent` | number | Percentage of warmup emails that will receive automated replies to simulate natural conversation; must be between 1 and 100. |
| `warmupSkipWeekends` | boolean | Skip sending warmup emails on Saturday and Sunday to simulate natural business communication patterns. |

## Native endpoint

Through the native ManyReach API, this operation is `GET https://api.manyreach.com/api/v2/senders` (base URL `https://api.manyreach.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-senders.md) for the provider-specific parameters and requirements.

