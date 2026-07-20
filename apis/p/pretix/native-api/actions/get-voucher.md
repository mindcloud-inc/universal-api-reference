# Get Voucher with pretix

Retrieves a voucher from pretix.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizers/:organizer/events/:event/vouchers/:voucher/`
- **Base URL:** `https://pretix.eu/api/v1`
- **Official documentation:** [Get Voucher](https://docs.pretix.eu/dev/api/resources/vouchers.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizer` | path | `string` | yes | pretix organizer slug. |
| `event` | path | `string` | yes | pretix event slug. |
| `voucher` | path | `string` | yes | pretix voucher ID. |
