# Create Contact with Moskit

Creates a new contact in Moskit.

## Endpoint

- **Method:** `POST`
- **Path:** `contacts`
- **Base URL:** `https://api.ms.prod.moskit.services/v2`
- **Official documentation:** [Create Contact](https://moskit.stoplight.io/docs/api-v2/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cpf` | body | `string` | no | Optional CPF for the contact. |
| `createdBy.id` | body | `number` | yes | Moskit user ID that owns the creation record. |
| `name` | body | `string` | yes | Contact name. |
| `notes` | body | `string` | no | Optional notes for the contact. |
| `responsible.id` | body | `number` | yes | Moskit user ID responsible for the contact. |
