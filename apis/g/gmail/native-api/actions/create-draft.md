# Create Draft with Google Mail

Creates a Gmail draft.

## Endpoint

- **Method:** `POST`
- **Path:** `/drafts`
- **Base URL:** `https://gmail.googleapis.com/gmail/v1/users/:userId`
- **Official documentation:** [Create Draft](https://developers.google.com/workspace/gmail/api/reference/rest/v1/users.drafts/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `to` | body | `string` | no | Recipient email address. Use a comma-separated list for multiple recipients. |
| `subject` | body | `string` | no | Draft subject line. |
| `bodyText` | body | `string` | no | Plain-text draft body. If both Body Text and Body HTML are provided, Body Text is rendered above Body HTML. |
| `bodyHtml` | body | `string` | no | HTML draft body. If both Body Text and Body HTML are provided, Body Text is rendered above Body HTML. |
| `cc` | body | `string` | no | Optional CC recipients. Use a comma-separated list. |
| `bcc` | body | `string` | no | Optional BCC recipients. Use a comma-separated list. |
| `from` | body | `string` | no | Optional sender header. Must be permitted by Gmail account configuration. |
| `replyTo` | body | `string` | no | Optional Reply-To address. |
| `threadId` | body | `string` | no | Optional Gmail thread ID when adding the draft to an existing thread. |
| `inReplyTo` | body | `string` | no | Optional RFC 2822 In-Reply-To header for threaded replies. |
| `references` | body | `string` | no | Optional RFC 2822 References header for threaded replies. |
