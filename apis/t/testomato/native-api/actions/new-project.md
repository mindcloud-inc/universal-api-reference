# New project with Testomato

Creates a new project in Testomato.

## Endpoint

- **Method:** `POST`
- **Path:** `/project/create`
- **Base URL:** `https://testomato.com/api`
- **Official documentation:** [New project](https://help.testomato.com/api/new-project)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `url` | body | `string` | yes |
| `addPresetChecks` | body | `boolean` | no |
