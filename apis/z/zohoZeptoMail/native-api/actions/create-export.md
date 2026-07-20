# Create Export with Zoho ZeptoMail

Creates a new export for Zoho ZeptoMail logs.

## Endpoint

- **Method:** `POST`
- **Path:** `:exportType/exports`
- **Base URL:** `https://api.zeptomail.com/v1.1`
- **Official documentation:** [Create Export](https://www.zoho.com/zeptomail/help/api/export-logs.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bcc` | body | `string` | no | BCC recipient filter for exports. |
| `bounce_category` | body | `string` | no | Bounce category filter for mail-log exports. |
| `cc` | body | `string` | no | CC recipient filter for exports. |
| `client_reference` | body | `string` | no | Client reference filter for exports. |
| `date_from` | body | `string` | no | Start date for the export window. |
| `date_to` | body | `string` | no | End date for the export window. |
| `dndType` | body | `string` | no | Suppression export type: email or domain. |
| `entity` | body | `string` | no | Activity-log entity to export. |
| `exportType` | path | `string` | yes | Export category to create. |
| `from` | body | `string` | no | Sender address to filter exports by. |
| `is_delivered` | body | `boolean` | no | Include delivered email logs in the export. |
| `is_hb` | body | `boolean` | no | Include hard bounce logs in the export. |
| `is_mailfailure` | body | `boolean` | no | Include processed failed email logs in the export. |
| `is_sb` | body | `boolean` | no | Include soft bounce logs in the export. |
| `mailagent_key` | body | `string` | no | Agent alias to export logs for. |
| `modified_by` | body | `string` | no | User who modified the exported activity entity. |
| `password` | body | `string` | no | Optional password to protect the exported file. |
| `subject` | body | `string` | no | Email subject filter for exports. |
| `to` | body | `string` | no | Recipient address to filter exports by. |
