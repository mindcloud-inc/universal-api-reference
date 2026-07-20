# Update Template with SignWell

Updates an existing template in SignWell.

## Endpoint

- **Method:** `PUT`
- **Path:** `/document_templates/:id`
- **Base URL:** `https://www.signwell.com/api/v1`
- **Official documentation:** [Update Template](https://developers.signwell.com/reference/put_api-v1-document-templates-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | — |
| `name` | body | `string` | no | Updated template name. |
| `subject` | body | `string` | no | Updated email subject for the template. |
| `message` | body | `string` | no | Updated request message for the template. |
