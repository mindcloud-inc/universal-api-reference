# Update Contact with Project Bubble

Updates an existing contact in Project Bubble.

## Endpoint

- **Method:** `PUT`
- **Path:** `/contacts/:contact_id`
- **Base URL:** `https://api.projectbubble.com/v2`
- **Official documentation:** [Update Contact](https://help.proprofsproject.com/managing-contacts)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `contact_id` | path | `string` | yes |
| `contact_name` | body | `string` | no |
