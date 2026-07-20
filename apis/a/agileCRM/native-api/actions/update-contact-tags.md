# Update Contact Tags with Agile CRM

Updates tags for a contact in Agile CRM.

## Endpoint

- **Method:** `PUT`
- **Path:** `/contacts/edit/tags`
- **Base URL:** `https://mindcloud.agilecrm.com/dev/api`
- **Official documentation:** [Update Contact Tags](https://github.com/agilecrm/rest-api#17-update-tags-value-by-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `list` | yes | Contact record to tag. |
| `tags[]` | body | `array<string>` | yes | Tags to add. Send as an array. |
