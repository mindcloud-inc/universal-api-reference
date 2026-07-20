# Update Tag with Cerbo

Updates an existing tag in Cerbo.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/tags/:tag_id`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [Update Tag](https://docs.cer.bo/#tag/Tags/operation/updateTag)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tag_id` | path | `number` | yes | ID of tag to update |
| `name` | body | `string` | yes | Name of the tag. The name must be unique. |
| `category` | body | `string` | yes | Category for the tag. |
| `description` | body | `string` | yes | Description for the tag. |
| `displays_on_dash` | body | `boolean` | yes | Display the tag under the associated patient photo block when the patient chart or encounter note is opened. |
| `note_displays_on_dashboard` | body | `boolean` | yes | Display the full text of any associated tag note in addition to showing the existence of the tag on the dashboard. This behavior is dependent on `displays_on_dash` being `true` as well. |
| `displays_on_calendar` | body | `boolean` | yes | Display in the scheduler interface when scheduling an appointment for a tagged patient. |
| `color` | body | `string` | yes | A valid six-digit hex code that defines the color for the tag. |
