# Create campaign with Vibrato

Creates a new campaign in Vibrato.

## Endpoint

- **Method:** `POST`
- **Path:** `/campaigns/`
- **Base URL:** `https://api.getvibrato.com/api/v1`
- **Official documentation:** [Create campaign](https://docs.getvibrato.com/api-reference/campaigns/create-a-new-campaign)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Campaign name. |
| `task_property_to_contact_field` | body | `object` | yes | Mapping from task property slugs to contact fields. |
| `task_template_uuid` | body | `string` | yes | Task template UUID. |
| `daily_availability[]` | body | `array<object>` | yes | Daily availability windows. |
| `timezone` | body | `string` | yes | Campaign timezone. |
| `paused` | body | `boolean` | no | Whether the campaign is paused. |
