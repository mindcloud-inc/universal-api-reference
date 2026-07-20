# Update Template with Pirsonal

Updates an existing template in Pirsonal.

## Endpoint

- **Method:** `POST`
- **Path:** `/api`
- **Base URL:** `https://app.pirsonal.com`
- **Official documentation:** [Update Template](https://app.pirsonal.com/docAPI#Template_Update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `templateID` | body | `string` | yes | ID of the template to update. |
| `update` | body | `object` | yes | TemplateUpdate_t object with fields to modify. |
