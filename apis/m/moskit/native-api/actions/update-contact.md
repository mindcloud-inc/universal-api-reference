# Update Contact with Moskit

Updates an existing contact in Moskit.

## Endpoint

- **Method:** `PUT`
- **Path:** `contacts/:id`
- **Base URL:** `https://api.ms.prod.moskit.services/v2`
- **Official documentation:** [Update Contact](https://moskit.stoplight.io/docs/api-v2/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cpf` | body | `string` | no | Optional CPF for the contact. |
| `createdBy.id` | body | `number` | yes | Moskit user ID that owns the creation record. |
| `id` | path | `number` | yes | Moskit contact ID. |
| `name` | body | `string` | yes | Contact name. |
| `responsible.id` | body | `number` | yes | Moskit user ID responsible for the contact. |
