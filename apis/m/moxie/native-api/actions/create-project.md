# Create Project with Moxie

Creates a new project in Moxie.

## Endpoint

- **Method:** `POST`
- **Path:** `/action/projects/create`
- **Base URL:** `https://pod01.withmoxie.com/api/public`
- **Official documentation:** [Create Project](https://help.withmoxie.com/en/articles/8160400-create-project)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Project name. |
| `clientName` | body | `string` | yes | Existing client name for the project. |
| `templateName` | body | `string` | no | Project template name to clone from. |
| `startDate` | body | `date` | no | Project start date. |
| `dueDate` | body | `date` | no | Project due date. |
| `portalAccess` | body | `string` | no | Portal access level for the project. |
| `showTimeWorkedInPortal` | body | `boolean` | no | Whether time worked should be visible in the client portal. |
| `feeSchedule` | body | `object` | no | Fee schedule object when not using a template. |
