# Update Calendar with Karma CRM

Updates an existing calendar in Karma CRM.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v3/calendars/:id.json`
- **Base URL:** `https://app.karmacrm.com`
- **Official documentation:** [Update Calendar](https://docs.karmacrm.com/#update-a-calendar)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `calendar` | body | `object` | yes | Calendar payload object containing title, color, privacy flags, and calendar_users changes. |
| `id` | path | `number` | yes | The ID of the calendar to update. |
