# Update Issue with Sifter

Updates an existing issue in Sifter.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:project_id/issues/:issue_id`
- **Base URL:** `https://{subdomain}.sifterapp.com/api`
- **Official documentation:** [Update Issue](https://sifterapp.com/developer/documentation/comments/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `assignee_name` | body | `string` | no |
| `body` | body | `string` | no |
| `category_name` | body | `string` | no |
| `internal` | body | `boolean` | no |
| `issue_id` | path | `number` | yes |
| `milestone_name` | body | `string` | no |
| `priority_name` | body | `string` | no |
| `project_id` | path | `number` | yes |
