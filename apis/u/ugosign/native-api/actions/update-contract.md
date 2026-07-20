# Update Contract with Ugosign

Updates an existing contract in Ugosign.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/contracts/:contract`
- **Base URL:** `https://app.ugosign.com/api`
- **Official documentation:** [Update Contract](https://app.ugosign.com/api/docs)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `allow_refusal` | body | `string` | no |
| `author_id` | body | `string` | no |
| `content` | body | `string` | no |
| `contract` | path | `string` | yes |
| `description` | body | `string` | no |
| `folder_id` | body | `string` | no |
| `footer` | body | `string` | no |
| `initials` | body | `string` | no |
| `reminder` | body | `string` | no |
| `title` | body | `string` | no |
