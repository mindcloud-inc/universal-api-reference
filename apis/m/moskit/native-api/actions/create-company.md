# Create Company with Moskit

Creates a new company in Moskit.

## Endpoint

- **Method:** `POST`
- **Path:** `companies`
- **Base URL:** `https://api.ms.prod.moskit.services/v2`
- **Official documentation:** [Create Company](https://moskit.stoplight.io/docs/api-v2/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cnpj` | body | `string` | no | Optional CNPJ for the company. |
| `createdBy.id` | body | `number` | yes | Moskit user ID that owns the creation record. |
| `domain` | body | `string` | no | Optional company domain. |
| `name` | body | `string` | yes | Company name. |
| `notes` | body | `string` | no | Optional notes for the company. |
| `responsible.id` | body | `number` | yes | Moskit user ID responsible for the company. |
