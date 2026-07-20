# Create Contact with Ugosign

Creates a new contact in Ugosign.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/contacts`
- **Base URL:** `https://app.ugosign.com/api`
- **Official documentation:** [Create Contact](https://app.ugosign.com/api/docs)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `city` | body | `string` | no |
| `country` | body | `string` | no |
| `email` | body | `string` | yes |
| `family_name` | body | `string` | no |
| `gender` | body | `string` | no |
| `given_name` | body | `string` | no |
| `organization_name` | body | `string` | no |
| `phone_number` | body | `string` | no |
| `position` | body | `string` | no |
| `postal_code` | body | `string` | no |
| `private_comment` | body | `string` | no |
| `street` | body | `string` | no |
| `street_2` | body | `string` | no |
| `website` | body | `string` | no |
