# Create Calendar with Karma CRM

Creates a new calendar in Karma CRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v3/calendars.json`
- **Base URL:** `https://app.karmacrm.com`
- **Official documentation:** [Create Calendar](https://docs.karmacrm.com/#create-a-calendar)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `calendar` | body | `object` | yes | Calendar payload object containing title, color, privacy flags, and optional calendar_users. |
