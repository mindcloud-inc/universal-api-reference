# Get Availability with Sprintful

Retrieves booking page availability from Sprintful.

## Endpoint

- **Method:** `GET`
- **Path:** `/availability/:slug`
- **Base URL:** `https://app.sprintful.com/api/v1`
- **Official documentation:** [Get Availability](https://support.sprintful.com/article/129-sprintful-for-developers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `slug` | path | `string` | yes | The Sprintful booking page slug. |
| `start_date` | query | `string` | no | Availability window start date. Sprintful format: DD-MM-YYY. |
| `end_date` | query | `string` | no | Availability window end date. Sprintful format: DD-MM-YYY. |
