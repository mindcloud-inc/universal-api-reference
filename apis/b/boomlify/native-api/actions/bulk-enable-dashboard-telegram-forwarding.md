# Bulk Enable Dashboard Telegram Forwarding with Boomlify

Bulk enables Telegram forwarding for owned mailboxes in Boomlify.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/emails/telegram-forwarding/bulk-enable`
- **Base URL:** `https://v1.boomlify.com`
- **Official documentation:** [Bulk Enable Dashboard Telegram Forwarding](https://boomlify.com/en/temp-mail-api-docs?endpoint=bulk-enable-dashboard-telegram-forwarding&tab=docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email_ids[]` | body | `array<string>` | yes | Dashboard email UUIDs to enable Telegram forwarding for. |
