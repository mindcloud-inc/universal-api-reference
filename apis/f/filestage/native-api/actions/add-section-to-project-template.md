# Add Section to Project Template with Filestage

Creates a section in a Filestage project template.

## Endpoint

- **Method:** `POST`
- **Path:** `/project-templates/{projectTemplateId}/sections`
- **Base URL:** `https://api.filestage.io/ext/v2`
- **Official documentation:** [Add Section to Project Template](https://developers.filestage.io/docs/api/651rufwgkc4fi-add-section-to-project-template)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectTemplateId` | path | `string` | yes | ID of the project template |
| `name` | body | `string` | yes | The name of the section. |
