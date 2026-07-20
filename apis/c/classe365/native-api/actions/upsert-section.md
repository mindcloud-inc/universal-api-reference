# Upsert Section with Classe365

Creates or updates a section in Classe365.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/academic`
- **Base URL:** `https://{username}.classe365.com`
- **Official documentation:** [Upsert Section](https://speca.io/classe365/academics#insert-update-section)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `class_id` | body | `string` | no | Class id. |
| `code` | body | `string` | no | Section code. |
| `name` | body | `string` | no | Section name. |
| `type` | body | `string` | no | Fixed value section. |
