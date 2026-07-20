# Update PDF Template with API Template

Updates an existing PDF template in API Template.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/update-template`
- **Base URL:** `https://rest.apitemplate.io`
- **Official documentation:** [Update PDF Template](https://apitemplate.io/apiv2/#tag/Template-Management/operation/update-template)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `template_id` | body | `string` | yes | Template ID to update. |
| `body` | body | `string` | no | Updated HTML body for the template. |
| `css` | body | `string` | no | Updated CSS for the template. |
