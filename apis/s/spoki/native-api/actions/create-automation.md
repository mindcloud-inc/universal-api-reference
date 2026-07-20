# Create Automation with Spoki

Creates an automation with steps, triggers, and optional automation groups.

## Endpoint

- **Method:** `POST`
- **Path:** `/automations/`
- **Base URL:** `https://api.spoki.com/api/1`
- **Official documentation:** [Create Automation](https://documenter.getpostman.com/view/21611004/UzBqnPvF)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Name of the automation. |
| `is_active` | body | `boolean` | no | Whether the automation should start active immediately. |
| `payload` | body | `object` | no | Optional advanced automation fields to merge into the provider request body, including steps, triggers, groups, and other supported Spoki fields. |
