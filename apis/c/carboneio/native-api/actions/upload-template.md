# Upload Template with Carbone.io

Creates a template in Carbone.io.

## Endpoint

- **Method:** `POST`
- **Path:** `/template`
- **Base URL:** `https://api.carbone.io`
- **Official documentation:** [Upload Template](https://carbone.io/documentation/developer/http-api/manage-templates.html#upload-a-template)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `category` | body | `string` | no | Category used to organize the template. |
| `comment` | body | `string` | no | Template comment. |
| `deployedAt` | body | `number` | no | UTC Unix timestamp that marks the deployed template version. |
| `expireAt` | body | `number` | no | UTC Unix timestamp after which the template is deleted. |
| `id` | body | `string` | no | Existing Template ID (64-bit) to append a new version to. Leave blank to create a new template ID. |
| `name` | body | `string` | no | Template name. |
| `sample[]` | body | `array<object>` | no | Sample data used in Carbone Studio for testing and development. |
| `tags[]` | body | `array<string>` | no | List of tags to assign to the template. |
| `template` | body | `string` | yes | Base64-encoded contents of the template file. |
| `versioning` | body | `boolean` | no | Enable template versioning for the uploaded template. |
