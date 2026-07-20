# Schedule Campaign with MailoPost

Schedules a MailoPost campaign for delivery.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/email/campaigns/:id/schedule`
- **Base URL:** `https://api.mailopost.ru/v1`
- **Official documentation:** [Schedule Campaign](https://mailopost.ru/api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | MailoPost campaign identifier. |
| `start_at` | body | `string` | no | Scheduled send date and time. |
| `time_zone` | body | `string` | no | MailoPost time zone name for the scheduled send. |
