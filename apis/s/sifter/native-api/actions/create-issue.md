# Create Issue with Sifter

Creates a new issue in Sifter.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:project_id/issues`
- **Base URL:** `https://{subdomain}.sifterapp.com/api`
- **Official documentation:** [Create Issue](https://sifterapp.com/developer/documentation/issues/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `assignee_name` | body | `string` | no | The assignee username or name from the project people list. |
| `body` | body | `string` | no | The issue description. |
| `category_name` | body | `string` | no | The category name from the project categories list. |
| `milestone_name` | body | `string` | no | The milestone name from the project milestones list. |
| `priority_name` | body | `string` | no | The priority name from Sifter, for example Normal. |
| `project_id` | path | `number` | yes | The Sifter project ID. |
| `subject` | body | `string` | yes | The issue title. |
