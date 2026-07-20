# Create Contract with Ugosign

Creates a new contract in Ugosign.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/contracts`
- **Base URL:** `https://app.ugosign.com/api`
- **Official documentation:** [Create Contract](https://app.ugosign.com/api/docs)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `allow_refusal` | body | `boolean` | no |
| `author_id` | body | `string` | yes |
| `content` | body | `string` | no |
| `description` | body | `string` | no |
| `file` | body | `file` | no |
| `folder_id` | body | `string` | no |
| `footer` | body | `string` | no |
| `initials` | body | `boolean` | no |
| `reminder` | body | `number` | no |
| `title` | body | `string` | yes |
