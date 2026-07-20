# List Project Categories with Sifter

Retrieves categories for a project from Sifter.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:project_id/categories`
- **Base URL:** `https://{subdomain}.sifterapp.com/api`
- **Official documentation:** [List Project Categories](https://sifterapp.com/developer/documentation/projects/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `number` | yes | The Sifter project ID. |
