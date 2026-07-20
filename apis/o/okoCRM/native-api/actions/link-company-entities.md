# Link company entities with OkoCRM

Links entities to a company in OkoCRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/companies/[:company_id]/link/`
- **Base URL:** `https://api.okocrm.com/v2`
- **Official documentation:** [Link company entities](https://okocrm.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_id` | path | `number` | yes | The OkoCRM company ID. |
| `contacts[][id]` | body | `string` | no | A contact ID to link to the company. |
| `leads[][id]` | body | `string` | no | A deal ID to link to the company. |
