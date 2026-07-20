# Create Sender with ManyReach

Creates a new sender in ManyReach.

## Endpoint

- **Method:** `POST`
- **Path:** `https://api.manyreach.com/api/v2/senders`
- **Base URL:** `https://api.manyreach.com`
- **Official documentation:** [Create Sender](https://api.manyreach.com/api#v2/tag/sender)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customImapPass` | body | `string` | yes | IMAP password. |
| `customImapPort` | body | `string` | yes | IMAP server port. |
| `customImapServer` | body | `string` | yes | IMAP server hostname. |
| `customImapUsername` | body | `string` | no | IMAP username. |
| `customSmtpPass` | body | `string` | yes | SMTP password. |
| `customSmtpPort` | body | `number` | yes | SMTP server port. |
| `customSmtpServer` | body | `string` | yes | SMTP server hostname. |
| `customSmtpUsername` | body | `string` | no | SMTP username. |
| `customWarmupTag` | body | `string` | no | Custom tag applied to warmup behavior. |
| `dailyLimit` | body | `number` | yes | Maximum emails the sender can send per day. |
| `dailyLimitIncrease` | body | `boolean` | no | Whether the daily limit increases automatically. |
| `dailyLimitIncreasePercent` | body | `number` | no | Percentage increase applied to the daily limit. |
| `dailyLimitIncreaseToMax` | body | `number` | no | Maximum daily limit when automatic increases are enabled. |
| `delayMin` | body | `number` | no | Delay in minutes between sent emails. |
| `email` | body | `string` | yes | Sender email address. |
| `firstName` | body | `string` | no | Sender first name. |
| `folder` | body | `string` | no | Folder used to organize the sender. |
| `fromName` | body | `string` | no | Display name shown in outgoing emails. |
| `lastName` | body | `string` | no | Sender last name. |
| `replyTo` | body | `string` | no | Reply-to email address. |
| `senderCustom1` | body | `string` | no | Custom sender field 1. |
| `senderCustom10` | body | `string` | no | Custom sender field 10. |
| `senderCustom2` | body | `string` | no | Custom sender field 2. |
| `senderCustom3` | body | `string` | no | Custom sender field 3. |
| `senderCustom4` | body | `string` | no | Custom sender field 4. |
| `senderCustom5` | body | `string` | no | Custom sender field 5. |
| `senderCustom6` | body | `string` | no | Custom sender field 6. |
| `senderCustom7` | body | `string` | no | Custom sender field 7. |
| `senderCustom8` | body | `string` | no | Custom sender field 8. |
| `senderCustom9` | body | `string` | no | Custom sender field 9. |
| `signature` | body | `string` | no | Email signature HTML. |
| `trackingDomain` | body | `string` | no | Custom tracking domain for the sender. |
| `warmup` | body | `boolean` | no | Whether sender warmup is enabled. |
| `warmupDailyLimit` | body | `number` | no | Daily sending limit used during warmup. |
| `warmupDailyLimitIncrease` | body | `boolean` | no | Whether the warmup daily limit increases automatically. |
| `warmupDailyLimitIncreasePercent` | body | `number` | no | Percentage increase applied to the warmup daily limit. |
| `warmupDailyLimitIncreaseToMax` | body | `number` | no | Maximum warmup daily limit when automatic increases are enabled. |
| `warmupReplyPercent` | body | `number` | no | Expected reply percentage during warmup. |
| `warmupSkipWeekends` | body | `boolean` | no | Whether warmup activity skips weekends. |
