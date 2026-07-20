# List Attendees with Corsizio

Retrieves attendees from a Corsizio account.

## Endpoint

- **Method:** `GET`
- **Path:** `/attendees`
- **Base URL:** `https://api.corsizio.com/v1`
- **Official documentation:** [List Attendees](https://help.corsizio.com/article/43-api-get-attendees-list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status` | query | `string` | no | Attendee status filter such as active, waiting, paid, owing, or any. Send multiple values as a string separated by `,`. |
| `date` | query | `string` | no | Date range like 2026-03-01:2026-03-31. |
| `event` | query | `list<string>` | no | Filter by a specific event ID. |
| `coupon` | query | `string` | no | Filter by a specific coupon code. |
| `search` | query | `string` | no | Search by attendee name, email, phone, or exact attendee ID. |
| `include` | query | `list<string>` | no | Comma-separated values: payment, activity, details. Accepted values: `activity`, `details`, `payment`. Send multiple values as a string separated by `,`. |
| `expand` | query | `list<string>` | no | Comma-separated values: event, account. Accepted values: `account`, `event`. Send multiple values as a string separated by `,`. |
