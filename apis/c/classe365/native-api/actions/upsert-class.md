# Upsert Class with Classe365

Creates or updates a class in Classe365.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/academic`
- **Base URL:** `https://{username}.classe365.com`
- **Official documentation:** [Upsert Class](https://speca.io/classe365/academics#insert-update-class)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | body | `string` | no | Class code. |
| `department_id` | body | `string` | no | Department id. |
| `name` | body | `string` | no | Class name. |
| `type` | body | `string` | no | Fixed value class. |
