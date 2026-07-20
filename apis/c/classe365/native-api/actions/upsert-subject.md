# Upsert Subject with Classe365

Creates or updates a subject in Classe365.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/academic`
- **Base URL:** `https://{username}.classe365.com`
- **Official documentation:** [Upsert Subject](https://speca.io/classe365/academics#insert-update-subject)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `class_id` | body | `string` | no | Class id. |
| `code` | body | `string` | no | Subject code. |
| `name` | body | `string` | no | Subject name. |
| `section_id` | body | `string` | no | Section id. |
| `type` | body | `string` | no | Fixed value subject. |
