# Duplicate Workspace Template with Abyssale

Duplicates a workspace template into an Abyssale project.

## Endpoint

- **Method:** `POST`
- **Path:** `/workspace-templates/:companyTemplateId/use`
- **Base URL:** `https://api.abyssale.com`
- **Official documentation:** [Duplicate Workspace Template](https://developers.abyssale.com/rest-api/workspace-templates)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyTemplateId` | path | `string` | yes | Workspace template UUID to duplicate |
| `project_id` | body | `string` | yes | Target project ID where the template will be duplicated |
