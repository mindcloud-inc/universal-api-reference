# List Emails with Zoho Mail

Retrieves email messages from Zoho Mail.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:accountId/messages/view`
- **Base URL:** `https://mail.zoho.com/api`
- **Official documentation:** [List Emails](https://www.zoho.com/mail/help/api/get-emails-list.html)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `string` | yes | Account identifier returned by List Accounts. |
| `folderId` | query | `string` | no | Folder identifier returned by List Folders. |
| `status` | query | `string` | no | Filter emails by read or unread status. |
| `labelid` | query | `string` | no | Filter emails by label identifier. |
| `threadId` | query | `string` | no | Filter emails by thread identifier. |
| `flagid` | query | `number` | no | Filter emails by flag type identifier. |
| `includeto` | query | `boolean` | no | Include recipient details in the response. |
| `includesent` | query | `boolean` | no | Include sent emails in the response. |
| `includearchive` | query | `boolean` | no | Include archived emails in the response. |
| `attachedMails` | query | `boolean` | no | Only return emails with attachments when true. |
| `inlinedMails` | query | `boolean` | no | Only return emails with inline images when true. |
| `flaggedMails` | query | `boolean` | no | Only return flagged emails when true. |
| `respondedMails` | query | `boolean` | no | Only return emails with replies when true. |
| `threadedMails` | query | `boolean` | no | Only return threaded emails when true. |
