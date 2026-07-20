# Deliver Campaign with MailoPost

Delivers a MailoPost campaign immediately.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/email/campaigns/:id/deliver`
- **Base URL:** `https://api.mailopost.ru/v1`
- **Official documentation:** [Deliver Campaign](https://mailopost.ru/api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | MailoPost campaign identifier. |
