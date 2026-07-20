# Update Prospect Status with SmartReach

Updates prospect status in SmartReach.

## Endpoint

- **Method:** `PUT`
- **Path:** `/prospects/prospect_status_change`
- **Base URL:** `https://api.smartreach.io/api/v3`
- **Official documentation:** [Update Prospect Status](https://help.smartreach.io/reference/put_prospects-prospect-status-change)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign_ids[]` | body | `array<string>` | yes | Campaign IDs associated with the prospect status update. |
| `prospect_ids[]` | body | `array<string>` | yes | Prospect IDs to update. |
| `prospect_status` | body | `string` | yes | Target prospect status to apply. |
| `will_resume_at` | body | `number` | no | Resume timestamp when using resume_later. |
| `will_resume_at_tz` | body | `string` | no | Timezone for the resume timestamp. |
