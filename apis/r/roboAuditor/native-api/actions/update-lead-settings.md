# Update Lead Settings with RoboAuditor

## Endpoint

- **Method:** `POST`
- **Path:** `/lead-settings`
- **Base URL:** `https://app.siteauditor.com/api`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `never_bounce` | body | `number` | no | Enable or disable real-time email validation (1 or 0). |
| `email_address` | body | `number` | no | Enable blocking specific email addresses (1 or 0). |
| `email_domain` | body | `number` | no | Enable blocking specific email domains (1 or 0). |
| `whitelist_radio` | body | `number` | no | Enable URL blacklisting (1 or 0). |
| `add_emailalert` | body | `number` | no | Enable email notifications for team members (1 or 0). |
| `whitelist_urls[]` | body | `array<string>` | no | Array of URLs to block. |
| `block_emails[]` | body | `array<string>` | no | Array of blocked email addresses. |
| `block_domains[]` | body | `array<string>` | no | Array of blocked email domains. |
| `alert_emails[]` | body | `array<string>` | no | Array of emails that receive notifications. |
