# Get Budget Metadata with Procore

Retrieves budget metadata from Procore.

## Endpoint

- **Method:** `GET`
- **Path:** `/rest/v1.0/projects/:project_id/budget`
- **Base URL:** `https://api.procore.com`
- **Official documentation:** [Get Budget Metadata](https://developers.procore.com/reference/rest/budget#show-budget-meta-data)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Unique identifier for the project. |
