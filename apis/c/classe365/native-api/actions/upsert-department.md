# Upsert Department with Classe365

Creates or updates a department in Classe365.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/academic`
- **Base URL:** `https://{username}.classe365.com`
- **Official documentation:** [Upsert Department](https://speca.io/classe365/academics#insert-department)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Department name. |
| `id` | body | `string` | no | Existing department ID to update. Omit to create a new department. |
