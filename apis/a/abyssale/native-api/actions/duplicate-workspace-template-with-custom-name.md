# Duplicate Workspace Template With Custom Name with Abyssale

Duplicates a workspace template into an Abyssale project with a custom name.

## Endpoint

- **Method:** `POST`
- **Path:** `/workspace-templates/:companyTemplateId/use`
- **Base URL:** `https://api.abyssale.com`
- **Official documentation:** [Duplicate Workspace Template With Custom Name](https://developers.abyssale.com/rest-api/workspace-templates)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyTemplateId` | path | `string` | yes | Workspace template UUID to duplicate |
| `name` | body | `string` | yes | Optional custom name for the duplicated template |
| `project_id` | body | `string` | yes | Target project ID where the template will be duplicated |
