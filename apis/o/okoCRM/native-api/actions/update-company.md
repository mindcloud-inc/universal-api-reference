# Update company with OkoCRM

Updates an existing company in OkoCRM.

## Endpoint

- **Method:** `PUT`
- **Path:** `/companies/[:company_id]/`
- **Base URL:** `https://api.okocrm.com/v2`
- **Official documentation:** [Update company](https://okocrm.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_id` | path | `number` | yes | The OkoCRM company ID. |
| `emails[][email]` | body | `string` | no | One email address to attach to the company. |
| `name` | body | `string` | no | Updated company name. |
| `phones[][phone]` | body | `string` | no | One phone number to attach to the company. |
