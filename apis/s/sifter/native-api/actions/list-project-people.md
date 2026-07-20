# List Project People with Sifter

Retrieves assigned people for a project from Sifter.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:project_id/people`
- **Base URL:** `https://{subdomain}.sifterapp.com/api`
- **Official documentation:** [List Project People](https://sifterapp.com/developer/documentation/projects/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `number` | yes | The Sifter project ID. |
