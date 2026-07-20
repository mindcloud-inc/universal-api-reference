# Update Template with Carbone.io

Updates a template in Carbone.io.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/template/[:templateId-or-versionId]`
- **Base URL:** `https://api.carbone.io`
- **Official documentation:** [Update Template](https://carbone.io/documentation/developer/http-api/manage-templates.html#patch-a-template)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `category` | body | `string` | no | Category used to organize the template. |
| `comment` | body | `string` | no | Template comment. |
| `deployedAt` | body | `number` | no | UTC Unix timestamp that marks the deployed template version. |
| `expireAt` | body | `number` | no | UTC Unix timestamp after which the template is deleted. |
| `name` | body | `string` | no | Template name. |
| `tags[]` | body | `array<string>` | no | List of tags to assign to the template. |
| `templateId-or-versionId` | path | `string` | yes | Template ID (64-bit) or Version ID (SHA-256) to update. |
