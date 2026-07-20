# Update Template with PostGrid Print & Mail

Updates a template in PostGrid Print & Mail.

## Endpoint

- **Method:** `POST`
- **Path:** `/templates/{{id}}`
- **Base URL:** `https://api.postgrid.com/print-mail/v1`
- **Official documentation:** [Update Template](https://postgrid.readme.io/reference/templates_update-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | — |
| `html` | body | `string` | no | The updated HTML content for the template. |
| `description` | body | `string` | no | An optional updated description visible in the API and dashboard. |
| `metadata` | body | `object` | no | Updated custom metadata for this template. |
