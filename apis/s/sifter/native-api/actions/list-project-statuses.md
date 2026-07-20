# List Project Statuses with Sifter

Retrieves statuses for a project from Sifter.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:project_id/statuses`
- **Base URL:** `https://{subdomain}.sifterapp.com/api`
- **Official documentation:** [List Project Statuses](https://sifterapp.com/developer/documentation/statuses/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `number` | yes | The Sifter project ID. |
