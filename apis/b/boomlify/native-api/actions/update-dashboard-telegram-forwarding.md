# Update Dashboard Telegram Forwarding with Boomlify

Updates Telegram forwarding for an owned mailbox in Boomlify.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/emails/{id}/telegram-forwarding`
- **Base URL:** `https://v1.boomlify.com`
- **Official documentation:** [Update Dashboard Telegram Forwarding](https://boomlify.com/en/temp-mail-api-docs?endpoint=update-dashboard-telegram-forwarding&tab=docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Boomlify dashboard email UUID. |
| `is_enabled` | body | `boolean` | yes | Whether Telegram forwarding should be enabled. |
