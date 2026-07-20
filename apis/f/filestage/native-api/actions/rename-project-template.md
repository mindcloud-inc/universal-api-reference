# Rename Project Template with Filestage

Updates a project template name in Filestage.

## Endpoint

- **Method:** `PUT`
- **Path:** `/project-templates/{projectTemplateId}`
- **Base URL:** `https://api.filestage.io/ext/v2`
- **Official documentation:** [Rename Project Template](https://developers.filestage.io/docs/api/tgmtwbgtrfefq-rename-project-template)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectTemplateId` | path | `string` | yes | ID of the project template |
| `name` | body | `string` | yes | The name of the project template. |
