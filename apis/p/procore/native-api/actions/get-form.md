# Get Form with Procore

Retrieves a form from Procore.

## Endpoint

- **Method:** `GET`
- **Path:** `/rest/v1.0/projects/:project_id/forms/:id`
- **Base URL:** `https://api.procore.com`
- **Official documentation:** [Get Form](https://developers.procore.com/reference/rest/forms#show-form)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Unique identifier for the form. |
| `project_id` | path | `string` | yes | Unique identifier for the project. |
