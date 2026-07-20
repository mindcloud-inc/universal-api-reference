# Get Webhook Test Data with PlatoForms

Retrieves webhook test data for a form from PlatoForms.

## Endpoint

- **Method:** `GET`
- **Path:** `/form/{{form_identifier}}/webhook/`
- **Base URL:** `https://api.platoforms.com/v4`
- **Official documentation:** [Get Webhook Test Data](https://apidocs.platoforms.com/#operation/form_webhook_list)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `form_identifier` | path | `string` | yes |
