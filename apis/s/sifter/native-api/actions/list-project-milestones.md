# List Project Milestones with Sifter

Retrieves milestones for a project from Sifter.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:project_id/milestones`
- **Base URL:** `https://{subdomain}.sifterapp.com/api`
- **Official documentation:** [List Project Milestones](https://sifterapp.com/developer/documentation/projects/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `number` | yes | The Sifter project ID. |
