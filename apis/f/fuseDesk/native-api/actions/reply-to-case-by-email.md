# Reply to Case by Email with FuseDesk

Sends an email reply for an existing FuseDesk case.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/cases/:caseId/reply`
- **Base URL:** `https://{appName}.fusedesk.com`
- **Official documentation:** [Reply to Case by Email](https://documenter.getpostman.com/view/11014835/SztBc8ix#209dae86-c3c5-404c-aaea-d21e9c551b45)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bcc` | body | `string` | no | Comma-separated BCC recipient addresses. |
| `body` | body | `string` | yes | Plain-text reply body. |
| `caseId` | path | `number` | yes | The FuseDesk case ID to reply to. |
| `cc` | body | `string` | no | Comma-separated CC recipient addresses. |
| `from` | body | `string` | no | Sender email address. |
| `html` | body | `string` | no | HTML reply body. |
| `templateid` | body | `number` | no | Optional FuseDesk email template ID. |
| `to` | body | `string` | no | Recipient email address. |
