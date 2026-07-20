# Reject Time Entry with Beebole

Rejects a time entry in Beebole.

## Endpoint

- **Method:** `POST`
- **Base URL:** `https://beebole-apps.com/api/v2`
- **Official documentation:** [Reject Time Entry](https://beebole.com/help/api#reject-time-entry)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `person.id` | body | `number` | no | Optional person identifier when rejecting a date range. |
| `from` | body | `string` | no | Optional range start date in YYYY-MM-DD format. |
| `to` | body | `string` | no | Optional range end date in YYYY-MM-DD format. |
| `id` | body | `number` | no | Optional time entry identifier when rejecting one entry. |
| `date` | body | `string` | no | Optional time entry date in YYYY-MM-DD format when rejecting one entry. |
| `memo` | body | `string` | yes | The rejection reason sent to the employee via email. |
