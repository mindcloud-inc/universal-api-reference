# Update Time Off Blocked Period with TalentHR

Updates an existing blocked time off period in TalentHR.

## Endpoint

- **Method:** `PUT`
- **Path:** `/blocked-time-offs/:objectId`
- **Base URL:** `https://pubapi.talenthr.io/v1`
- **Official documentation:** [Update Time Off Blocked Period](https://apidocs.talenthr.io/#55e963ae-0331-4086-bd7a-972088c3a42c)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `objectId` | path | `number` | yes | Blocked time off ID. |
| `start_date` | body | `string` | yes | Blocked period start date in YYYY-MM-DD format. |
| `end_date` | body | `string` | yes | Blocked period end date in YYYY-MM-DD format. |
| `is_active` | body | `boolean` | yes | Whether the blocked period is active. |
| `timeoff_type[]` | body | `array<number>` | no | Optional array of time off type IDs. Leave empty to apply to all types. |
