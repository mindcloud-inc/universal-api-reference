# Update Address with Starshipit

## Endpoint

- **Method:** `POST`
- **Path:** `/addressbook/update`
- **Base URL:** `https://api.starshipit.com/api`
- **Official documentation:** [Update Address](https://api-docs.starshipit.com/#4ff9ae6f-fadb-4c50-9087-467c2e336f93)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | body | `number` | no |
| `address.code` | body | `string` | no |
| `address.name` | body | `string` | no |
| `address.company` | body | `string` | no |
| `address.post_code` | body | `string` | no |
| `address.street` | body | `string` | no |
| `address.suburb` | body | `string` | no |
| `address.city` | body | `string` | no |
| `address.state` | body | `string` | no |
| `address.country` | body | `string` | no |
| `address.phone` | body | `string` | no |
| `address.instructions` | body | `string` | no |
| `address.building` | body | `string` | no |
| `address.email` | body | `string` | no |
| `address.carrier` | body | `number` | no |
| `address.signature_required` | body | `boolean` | no |
