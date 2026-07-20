# Update Company with Moskit

Updates an existing company in Moskit.

## Endpoint

- **Method:** `PUT`
- **Path:** `companies/:id`
- **Base URL:** `https://api.ms.prod.moskit.services/v2`
- **Official documentation:** [Update Company](https://moskit.stoplight.io/docs/api-v2/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cnpj` | body | `string` | no | Optional CNPJ for the company. |
| `createdBy.id` | body | `number` | yes | Moskit user ID that owns the creation record. |
| `domain` | body | `string` | no | Optional company domain. |
| `id` | path | `number` | yes | Moskit company ID. |
| `name` | body | `string` | yes | Company name. |
| `responsible.id` | body | `number` | yes | Moskit user ID responsible for the company. |
