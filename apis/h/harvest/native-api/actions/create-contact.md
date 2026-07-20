# Create Contact with Harvest

Creates a new contact in Harvest.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/contacts`
- **Base URL:** `https://api.harvestapp.com`
- **Official documentation:** [Create Contact](https://help.getharvest.com/api-v2/clients-api/clients/contacts/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `client_id` | body | `number` | yes |
| `title` | body | `string` | no |
| `first_name` | body | `string` | yes |
| `last_name` | body | `string` | no |
| `email` | body | `string` | no |
| `phone_office` | body | `string` | no |
| `phone_mobile` | body | `string` | no |
| `fax` | body | `string` | no |
