# Update Contact with Bland AI

Updates an existing contact in Bland AI.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/contacts/{contact_id}`
- **Base URL:** `https://api.bland.ai`
- **Official documentation:** [Update Contact](https://docs.bland.ai/api-v1/patch/contacts-id)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `contact_id` | path | `string` | yes |
| `name` | body | `string` | no |
| `email` | body | `string` | no |
| `external_id` | body | `string` | no |
| `metadata` | body | `object` | no |
