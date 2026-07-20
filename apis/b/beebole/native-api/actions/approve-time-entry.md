# Approve Time Entry with Beebole

Approves a time entry in Beebole.

## Endpoint

- **Method:** `POST`
- **Base URL:** `https://beebole-apps.com/api/v2`
- **Official documentation:** [Approve Time Entry](https://beebole.com/help/api#approve-time-entry)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `person.id` | body | `number` | no | Optional person identifier when approving a date range. |
| `from` | body | `string` | no | Optional range start date in YYYY-MM-DD format. |
| `to` | body | `string` | no | Optional range end date in YYYY-MM-DD format. |
| `id` | body | `number` | no | Optional time entry identifier when approving one entry. |
| `date` | body | `string` | no | Optional time entry date in YYYY-MM-DD format when approving one entry. |
