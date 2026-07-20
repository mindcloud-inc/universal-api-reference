# Retrieve Process with Lokalise

Retrieves a process from a Lokalise project.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:project_id/processes/:process_id`
- **Base URL:** `https://api.lokalise.com/api2`
- **Official documentation:** [Retrieve Process](https://developers.lokalise.com/reference/retrieve-a-process)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `process_id` | path | `string` | no | Lokalise process identifier. |
| `project_id` | path | `string` | no | Lokalise project identifier. |
