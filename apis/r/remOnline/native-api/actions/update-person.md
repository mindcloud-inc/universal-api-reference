# Update Person with RemOnline

Updates an existing person in RemOnline.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v2/contacts/people/:person_id`
- **Base URL:** `https://api.roapp.io`
- **Official documentation:** [Update Person](https://roappua.readme.io/reference/update-person)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `person_id` | path | `number` | yes | ID of the person. |
| `notes` | body | `string` | no | Notes text. |
| `first_name` | body | `string` | no | Person first name. |
