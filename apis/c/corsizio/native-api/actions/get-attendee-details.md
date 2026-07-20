# Get Attendee Details with Corsizio

Retrieves an attendee from Corsizio by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/attendees/:id`
- **Base URL:** `https://api.corsizio.com/v1`
- **Official documentation:** [Get Attendee Details](https://help.corsizio.com/article/44-api-get-attendee-details)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `list<string>` | yes | The attendee ID to request. |
| `include` | query | `list<string>` | no | Comma-separated values: payment, activity, details. Accepted values: `activity`, `details`, `payment`. Send multiple values as a string separated by `,`. |
| `expand` | query | `list<string>` | no | Comma-separated values: event, account. Accepted values: `account`, `event`. Send multiple values as a string separated by `,`. |
