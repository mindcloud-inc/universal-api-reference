# Schedule Email Campaign Activity with Constant Contact

Schedules an email campaign activity in Constant Contact.

## Endpoint

- **Method:** `POST`
- **Path:** `/emails/activities/:campaign_activity_id/schedules`
- **Base URL:** `https://api.cc.email/v3`
- **Official documentation:** [Schedule Email Campaign Activity](https://developer.constantcontact.com/api_guide/email_campaign_create_schedule.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign_activity_id` | path | `string` | yes | The unique ID for the email campaign activity to schedule. |
| `scheduled_date` | body | `string` | yes | ISO-8601 send datetime, or "0" to send immediately. |
