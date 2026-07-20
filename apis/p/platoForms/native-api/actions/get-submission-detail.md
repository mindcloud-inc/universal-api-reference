# Get Submission Detail with PlatoForms

Retrieves detailed submission data from PlatoForms.

## Endpoint

- **Method:** `GET`
- **Path:** `/submission/{{submission_identifier}}/`
- **Base URL:** `https://api.platoforms.com/v4`
- **Official documentation:** [Get Submission Detail](https://apidocs.platoforms.com/#operation/submission_read)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `submission_identifier` | path | `string` | yes | — |
| `create_shared_urls` | query | `boolean` | no | Generate temporary shared download URLs for PDFs and attachments |
