# Link Associated Person with Column

## Endpoint

- **Method:** `POST`
- **Path:** `/entities/:entity_id/associated-persons`
- **Base URL:** `https://api.column.com`
- **Official documentation:** [Link Associated Person](https://column.com/docs/api/#entity/link-associated-person)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entity_id` | path | `string` | yes | ID of the business entity. |
| `person_entity_id` | body | `string` | yes | ID of the person entity to associate. |
| `roles[]` | body | `array<string>` | yes | Roles of the person in the business. |
| `title_in_business` | body | `string` | no | Job title or role of the person in the business. |
