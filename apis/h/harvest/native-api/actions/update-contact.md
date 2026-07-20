# Update Contact with Harvest

Updates an existing contact in Harvest.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v2/contacts/:id`
- **Base URL:** `https://api.harvestapp.com`
- **Official documentation:** [Update Contact](https://help.getharvest.com/api-v2/clients-api/clients/contacts/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `client_id` | body | `number` | no |
| `id` | path | `number` | yes |
| `title` | body | `string` | no |
| `first_name` | body | `string` | no |
| `last_name` | body | `string` | no |
| `email` | body | `string` | no |
| `phone_office` | body | `string` | no |
| `phone_mobile` | body | `string` | no |
| `fax` | body | `string` | no |
