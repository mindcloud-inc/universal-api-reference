# Update Person with Simplicate

## Endpoint

- **Method:** `PUT`
- **Path:** `/crm/person/:id`
- **Base URL:** `https://{subdomain}/api/v2`
- **Official documentation:** [Update Person](https://developer.simplicate.com/docs/api/v2/reference/update-crm-person/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | no | The person's email address |
| `family_name` | body | `string` | no | The person's family name |
| `first_name` | body | `string` | no | The person's first name |
| `id` | path | `string` | yes | The person's id |
| `note` | body | `string` | no | A note for the person |
