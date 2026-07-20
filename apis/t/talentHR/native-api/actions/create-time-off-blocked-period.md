# Create Time Off Blocked Period with TalentHR

Creates a new blocked time off period in TalentHR.

## Endpoint

- **Method:** `POST`
- **Path:** `/blocked-time-offs`
- **Base URL:** `https://pubapi.talenthr.io/v1`
- **Official documentation:** [Create Time Off Blocked Period](https://apidocs.talenthr.io/#74189047-c354-4de8-b879-bcb08e2f03cd)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start_date` | body | `string` | yes | Blocked period start date in YYYY-MM-DD format. |
| `end_date` | body | `string` | yes | Blocked period end date in YYYY-MM-DD format. |
| `is_active` | body | `boolean` | yes | Whether the blocked period is active. |
| `timeoff_type[]` | body | `array<number>` | no | Optional array of time off type IDs. Leave empty to apply to all types. |
