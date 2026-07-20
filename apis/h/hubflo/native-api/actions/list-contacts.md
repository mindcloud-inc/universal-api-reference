# List Contacts with Hubflo

Retrieves all contact records from Hubflo.

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts`
- **Base URL:** `https://app.hubflo.com/api/v2`
- **Official documentation:** [List Contacts](https://hubflo.readme.io/reference/get_api-v2-contacts)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `company_id` | query | `string` | no |
| `contact_id` | query | `string` | no |
| `email` | query | `string` | no |
| `linkedin` | query | `string` | no |
| `owner_id` | query | `string` | no |
| `page` | query | `number` | no |
| `phone` | query | `string` | no |
| `project_id` | query | `string` | no |
| `per_page` | query | `number` | no |
