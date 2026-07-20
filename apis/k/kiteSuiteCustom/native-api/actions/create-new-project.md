# Create new project with Kite Suite

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/project`
- **Base URL:** `https://api.kitesuite.com`
- **Official documentation:** [Create new project](https://api.kitesuite.com/swagger/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `projectName` | body | `string` | no |
| `projectType` | body | `string` | no |
| `projectLead` | body | `string` | no |
| `avatar` | body | `string` | no |
| `description` | body | `string` | no |
| `members[]` | body | `array` | no |
