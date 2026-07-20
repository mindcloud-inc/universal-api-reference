# Update Activity with Karma CRM

Updates an existing activity in Karma CRM.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v3/activities/:id.json`
- **Base URL:** `https://app.karmacrm.com`
- **Official documentation:** [Update Activity](https://docs.karmacrm.com/#update-an-activity)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The ID of the activity to update. |
| `activity` | body | `object` | yes | Activity payload object with the fields to update. |
