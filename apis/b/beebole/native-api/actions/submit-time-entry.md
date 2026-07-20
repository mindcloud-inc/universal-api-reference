# Submit Time Entry with Beebole

Submits a time entry for approval in Beebole.

## Endpoint

- **Method:** `POST`
- **Base URL:** `https://beebole-apps.com/api/v2`
- **Official documentation:** [Submit Time Entry](https://beebole.com/help/api#submit-time-entry)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `person.id` | body | `number` | no | Optional person identifier when submitting a date range. |
| `from` | body | `string` | no | Optional range start date in YYYY-MM-DD format. |
| `to` | body | `string` | no | Optional range end date in YYYY-MM-DD format. |
| `id` | body | `number` | no | Optional time entry identifier when submitting one entry. |
| `date` | body | `string` | no | Optional time entry date in YYYY-MM-DD format when submitting one entry. |
