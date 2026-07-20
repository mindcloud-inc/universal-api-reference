# Search Emails with FuseDesk

Finds emails in FuseDesk by matching search filters.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/emails/unassigned`
- **Base URL:** `https://{appName}.fusedesk.com`
- **Official documentation:** [Search Emails](https://documenter.getpostman.com/view/11014835/SztBc8ix#769f8f25-7063-4f31-8646-82fbd211b994)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bodylimit` | query | `number` | no | Maximum email body length to return. |
| `content` | query | `string` | no | Search text in the email body. |
| `from` | query | `string` | no | Sender email address to match. |
| `limit` | query | `number` | no | Maximum number of emails to return. |
| `offset` | query | `number` | no | Number of emails to skip. |
| `orderby` | query | `string` | no | Sort order expression. |
| `subject` | query | `string` | no | Search text in the email subject. |
